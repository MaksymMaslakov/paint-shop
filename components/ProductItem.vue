<template>
  <v-card class="mx-auto my-2" max-width="344">
    <v-img :src="item.imgUrl" height="200px" />

    <v-card-title>
      {{ item.title }}
    </v-card-title>
    <v-divider />

    <v-card-text>
      {{ item.descriptoion }}
    </v-card-text>

    <v-card-actions>
      <v-btn color="orange" text>
        Купить
      </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  props: ['item'],
  data: () => ({
    show: false
  })
}
</script>
