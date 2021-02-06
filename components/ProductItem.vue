<template>
  <v-list-item @click="$emit('toggle-drawer-details')">
    <template v-slot:default="{ active }">
      <v-list-item-content>
        <v-list-item-title v-text="item.title"></v-list-item-title>

        <v-list-item-subtitle
          class="text--primary"
          v-text="item.headline"
        ></v-list-item-subtitle>

        <v-list-item-subtitle v-text="item.subtitle"></v-list-item-subtitle>
      </v-list-item-content>

      <v-list-item-action>
        <v-list-item-action-text v-text="item.action"></v-list-item-action-text>

        <v-icon v-if="!active" color="grey lighten-1">
          mdi-star-outline
        </v-icon>

        <v-icon v-else color="yellow darken-3">
          mdi-star
        </v-icon>
      </v-list-item-action>
    </template>
  </v-list-item>
</template>

<script>
export default {
  props: ['item'],
  data: () => ({
    show: false
  })
}
</script>
