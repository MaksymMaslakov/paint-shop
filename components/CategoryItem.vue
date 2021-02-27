<template>
  <v-list-item
    link
    :to="`/categories/${category.id}`"
    max-width="644"
    max-height="200px"
    class="px-0 py-0 d-flex flex-no-wrap justify-space-between"
  >
    <v-img
      :src="category.imgUrl"
      height="200px"
      width="200px"
      class="d-inline-block category-image"
    />
    <div class="d-flex flex-column height-100">
      <v-card-title>
        {{ category.title }}
      </v-card-title>

      <v-card-subtitle v-if="category.subtitle">
        {{ category.subtitle }}
      </v-card-subtitle>

      <v-card-text v-if="category.descriptoion" class="overflow-y-hidden">
        {{ category.descriptoion }}
      </v-card-text>
    </div>
  </v-list-item>
</template>

<script>
export default {
  props: ['category']
}
</script>

<style scoped lang="scss">
.category-image:hover {
  opacity: 0.6;
  transition: opacity 0.3s ease-in-out;
}
</style>
