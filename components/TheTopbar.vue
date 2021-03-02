<template>
  <nav>
    <v-app-bar primary height="70px">
      <v-spacer />
      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-badge bordered color="error" :content="3" overlap>
        <v-btn icon>
          <v-icon>mdi-cart</v-icon>
        </v-btn>
      </v-badge>

      <v-btn text>
        EN
      </v-btn>
      <v-btn text>
        RU
      </v-btn>
      <v-btn text>
        UA
      </v-btn>
    </v-app-bar>

    <v-navigation-drawer
      v-model="drawer"
      app
      absolute
      permanent
      disable-resize-watcher
      width="244px"
    >
      <v-list-item class="logoContainer">
        <v-list-item-avatar>
          <v-img src="https://via.placeholder.com/50x50" />
        </v-list-item-avatar>

        <v-list-item-content>
          <v-list-item-title>LOGO</v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider />

      <v-list>
        <v-list-item v-for="item in navItems" :key="item.title" link :to="item.route" class="navItem">
          <v-list-item-icon>
            <v-icon v-if="item.icon">
              {{ item.icon }}
            </v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>
              {{ item.title }}
            </v-list-item-title>
          </v-list-item-content>
          <v-list v-if="item.options" class="d-none">
            <v-list-item
              v-for="(option, index) in item.options"
              :key="index"
            >
              <v-list-item-title>{{ option.title }}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-list-item>
      </v-list>

      <template #append>
        <v-layout justify-space-around class="mb-4">
          <v-tooltip
            v-for="({ icon, color, number, title }, i) in contactItems"
            :key="i"
            top
          >
            <template v-slot:activator="{ on, attrs }">
              <v-btn
                icon
                link
                large
                v-bind="attrs"
                :href="`tel:${number}`"
                v-on="on"
              >
                <v-icon :color="color">
                  {{ icon }}
                </v-icon>
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
        { icon: 'mdi-home', title: 'Главная', route: '/' },
        {
          icon: 'mdi-format-paint',
          title: 'Товары',
          route: '/products',
          options: [
            { title: 'Шпаклевка', route: '/products?category=putty' },
            { title: 'Краска', route: '/products?category=paint' },
            { title: 'Лак', route: '/products?category=varnish' }
          ]
        },
        { icon: 'mdi-account-supervisor', title: 'О нас', route: '/about' },
        { icon: 'mdi-palette', title: 'Палитра цветов', route: '/about1' },
        {
          icon: 'mdi-calculator-variant',
          title: 'Калькулятор',
          route: '/about3'
        },
        { icon: 'mdi-contacts', title: 'Контакты', route: '/contacts' },
        {
          icon: 'mdi-map-marker-right',
          title: 'Как нас найти',
          route: '/contacts2'
        }
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

<style lang="scss" scoped>
.logoContainer {
  height: 70px;
}

.navItem:hover {
  background: rgba(#0E3420, 0.8);
}
</style>
