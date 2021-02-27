<template>
  <v-list class="py-0">
    <category-item
      v-for="category in categories"
      :key="category.id"
      :category="category"
    />
  </v-list>
</template>

<script>
import CategoryItem from '@/components/CategoryItem'
export default {
  components: {
    CategoryItem
  },
  data: () => ({
    categories: [
      {
        id: '1',
        title: 'Интеръерная краска',
        subtitle: 'Какой-то пожзаголовок',
        imgUrl: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
        descriptoion: `I'm a thing. But, like most politicians, he promised more than he
            could deliver. You won't have time for sleeping, soldier, not with
            all the bed making you'll be doing. Then we'll go with that data
            file! Hey, you add a one and two zeros to that or we walk! You're
            going to do his laundry? I've got to find a way to escape.`
      },
      {
        id: '2',
        title: 'Лаки',
        subtitle: 'Какой-то пожзаголовок',
        imgUrl: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
        descriptoion: `I'm a thing. But, like most politicians, he promised more than he
            could deliver. You won't have time for sleeping, soldier, not with
            all the bed making you'll be doing. Then we'll go with that data
            file! Hey, you add a one and two zeros to that or we walk! You're
            going to do his laundry? I've got to find a way to escape.`
      },
      {
        id: '3',
        title: 'Лаки',
        subtitle: 'Какой-то пожзаголовок',
        imgUrl: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
        descriptoion: `I'm a thing. But, like most politicians, he promised more than he
            could deliver. You won't have time for sleeping, soldier, not with
            all the bed making you'll be doing. Then we'll go with that data
            file! Hey, you add a one and two zeros to that or we walk! You're
            going to do his laundry? I've got to find a way to escape.`
      },
      {
        id: '4',
        title: 'Лаки',
        subtitle: 'Какой-то пожзаголовок',
        imgUrl: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
        descriptoion: `I'm a thing. But, like most politicians, he promised more than he
            could deliver. You won't have time for sleeping, soldier, not with
            all the bed making you'll be doing. Then we'll go with that data
            file! Hey, you add a one and two zeros to that or we walk! You're
            going to do his laundry? I've got to find a way to escape.`
      }
    ]
  })
}
</script>
