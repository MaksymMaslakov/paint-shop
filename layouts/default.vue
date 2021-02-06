<template>
  <v-app>
    <!-- <v-navigation-drawer /> -->
    <navbar app />
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>

    <v-footer />
  </v-app>
</template>

<script>
import Navbar from '~/components/Navbar.vue'
export default {
  components: {
    Navbar
  }
}
</script>
