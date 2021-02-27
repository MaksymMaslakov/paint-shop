<template>
  <v-app>
    <the-topbar />
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
      <v-footer primary>
        <v-icon>mdi-home</v-icon>
      </v-footer>
    </v-main>
  </v-app>
</template>

<script>
import TheTopbar from '~/components/TheTopbar.vue'
export default {
  components: {
    TheTopbar
  }
}
</script>
