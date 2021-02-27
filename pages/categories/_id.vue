<template>
  <v-container>
    <v-row>
      <product-item
        v-for="product in products"
        :key="product.id"
        :item="product"
      />
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
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
  })
}
</script>
