<template>
  <v-list class="productList">
    <v-list-item-group
      v-model="selectedItem"
      color="primary"
    >
      <v-list-item
        v-for="product in products"
        :key="product.id"
        class="productList__item"
      >
        <v-list-item-icon class="productList__item__icon">
          <v-img :src="product.imgUrl" height="100" width="100" />
        </v-list-item-icon>
        <v-list-item-content>
          <v-list-item-title v-text="product.title" />
          <v-list-item-subtitle v-text="product.title" />
        </v-list-item-content>
      </v-list-item>
    </v-list-item-group>
  </v-list>
</template>

<script>
export default {
  data: () => ({
    selectedItem: 0,
    products: [
      {
        id: '1',
        title: 'Красная краска',
        imgUrl: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
        descriptoion: `Эта краска подходит для ... I'm a thing. But, like most politicians, he promised more than he
            could deliver. You won't have time for sleeping, soldier, not with
            all the bed making you'll be doing. Then we'll go with that data
            file! Hey, you add a one and two zeros to that or we walk! You're
            going to do his laundry? I've got to find a way to escape.`
      },
      {
        id: '2',
        title: 'Черная краска',
        imgUrl: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
        descriptoion: `Эта краска подходит для ... I'm a thing. But, like most politicians, he promised more than he
            could deliver. You won't have time for sleeping, soldier, not with
            all the bed making you'll be doing. Then we'll go with that data
            file! Hey, you add a one and two zeros to that or we walk! You're
            going to do his laundry? I've got to find a way to escape.`
      },
      {
        id: '7',
        title: 'Красная краска',
        imgUrl: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
        descriptoion: `Эта краска подходит для ... I'm a thing. But, like most politicians, he promised more than he
            could deliver. You won't have time for sleeping, soldier, not with
            all the bed making you'll be doing. Then we'll go with that data
            file! Hey, you add a one and two zeros to that or we walk! You're
            going to do his laundry? I've got to find a way to escape.`
      },
      {
        id: '6',
        title: 'Черная краска',
        imgUrl: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
        descriptoion: `Эта краска подходит для ... I'm a thing. But, like most politicians, he promised more than he
            could deliver. You won't have time for sleeping, soldier, not with
            all the bed making you'll be doing. Then we'll go with that data
            file! Hey, you add a one and two zeros to that or we walk! You're
            going to do his laundry? I've got to find a way to escape.`
      },
      {
        id: '8',
        title: 'Красная краска',
        imgUrl: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
        descriptoion: `Эта краска подходит для ... I'm a thing. But, like most politicians, he promised more than he
            could deliver. You won't have time for sleeping, soldier, not with
            all the bed making you'll be doing. Then we'll go with that data
            file! Hey, you add a one and two zeros to that or we walk! You're
            going to do his laundry? I've got to find a way to escape.`
      },
      {
        id: '9',
        title: 'Черная краска',
        imgUrl: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
        descriptoion: `Эта краска подходит для ... I'm a thing. But, like most politicians, he promised more than he
            could deliver. You won't have time for sleeping, soldier, not with
            all the bed making you'll be doing. Then we'll go with that data
            file! Hey, you add a one and two zeros to that or we walk! You're
            going to do his laundry? I've got to find a way to escape.`
      },
      {
        id: '11',
        title: 'Красная краска',
        imgUrl: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
        descriptoion: `Эта краска подходит для ... I'm a thing. But, like most politicians, he promised more than he
            could deliver. You won't have time for sleeping, soldier, not with
            all the bed making you'll be doing. Then we'll go with that data
            file! Hey, you add a one and two zeros to that or we walk! You're
            going to do his laundry? I've got to find a way to escape.`
      },
      {
        id: '12',
        title: 'Черная краска',
        imgUrl: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
        descriptoion: `Эта краска подходит для ... I'm a thing. But, like most politicians, he promised more than he
            could deliver. You won't have time for sleeping, soldier, not with
            all the bed making you'll be doing. Then we'll go with that data
            file! Hey, you add a one and two zeros to that or we walk! You're
            going to do his laundry? I've got to find a way to escape.`
      }
    ]
  }),
  watch: {
    selectedItem () {
      console.log(this.selectedItem)
    }
  },
  mounted () {
    this.selectedItem = this.products.indexOf((product) => {
      console.log(product.id, ' ?= ', this.$route.params.id)
      return product.id === this.$route.params.id
    })
  }
}
</script>

<style lang="scss" scoped>
.productList {
  padding-top: 0;

  &__item {
    height: 100px;
    padding-left: 0;

    &__icon {
      margin: 0;
    }
  }
}

</style>
