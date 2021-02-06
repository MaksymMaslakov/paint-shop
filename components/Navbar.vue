<template>
  <nav>
    <v-toolbar primary height="70px">
      <v-app-bar-nav-icon @click="drawer = !drawer" />
      <v-app-bar-title>ЛОГОТИП</v-app-bar-title>

      <v-spacer />
      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-badge bordered color="error" :content="3" overlap>
        <v-btn icon>
          <v-icon>mdi-cart</v-icon>
        </v-btn>
      </v-badge>
    </v-toolbar>

    <v-navigation-drawer
      app
      absolute
      temporary
      disable-resize-watcher
      v-model="drawer"
    >
      <v-list-item>
        <v-list-item-avatar>
          <v-img src="https://randomuser.me/api/portraits/men/78.jpg"></v-img>
        </v-list-item-avatar>

        <v-list-item-content>
          <v-list-item-title>John Leider</v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list>
        <v-list-item v-for="({ icon, text, route }, i) in navItems" :key="i" link :to="route">
          <v-list-item-icon>
            <v-icon>{{ icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ text }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <template #append>
        <v-layout justify-space-around class="mb-4">
          <v-tooltip
            top
            v-for="({ icon, color, number, title }, i) in contactItems"
            :key="i"
          >
            <template v-slot:activator="{ on, attrs }">
              <v-btn
                icon
                link
                large
                v-bind="attrs"
                v-on="on"
                :href="`tel:${number}`"
              >
                <v-icon :color="color">{{ icon }}</v-icon>
              </v-btn>
            </template>
            <span>{{ title }}</span>
          </v-tooltip>
        </v-layout>
      </template>
    </v-navigation-drawer>
  </nav>
</template>

<script>
export default {
  data () {
    return {
      drawer: false,
      navItems: [
        { icon: 'mdi-view-dashboard', text: 'Главная', route: '/' },
        { icon: 'mdi-apps', text: 'Товары', route: '/products' },
        { icon: 'mdi-account-group', text: 'О нас', route: '/about' },
        { icon: 'mdi-contacts', text: 'Контакты', route: '/contacts' }
      ],
      contactItems: [
        {
          icon: 'mdi-whatsapp',
          color: 'green',
          number: '+38099-123-45-67',
          title: 'Whatsapp'
        },
        {
          icon: 'mdi-telegram',
          color: 'blue',
          number: '+38099-123-45-67',
          title: 'Telegram'
        },
        {
          icon: 'mdi-phone-settings',
          color: 'purple',
          number: '+38099-123-45-67',
          title: 'Viber'
        }
      ]
    }
  }
}
</script>
