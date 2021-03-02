<template>
  <v-card
    width="500"
    tile
    class="productNav"
  >
    <product-list />
  </v-card>
  <!-- <v-container>
    <v-row>
      <product-item
        v-for="product in products"
        :key="product.id"
        :item="product"
      />
    </v-row>
  </v-container> -->
</template>

<script>
import ProductList from '../../components/ProductList.vue'
export default {
  components: {
    ProductList
  }
}
</script>

<style lang="scss" scoped>
.productNav {
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  overflow-y: scroll;
  padding-bottom: 60px;
}

</style>
