<template>
  <v-list two-line>
    <v-list-item-group v-model="selected" active-class="pink--text" multiple>
      <template v-for="(item, index) in items">
        <product-item
          :item="item"
          :key="item.title"
          @toggle-drawer-details="productDetailsDrawer = !productDetailsDrawer"
        />
        <v-divider v-if="index < items.length - 1" :key="index"></v-divider>
      </template>
    </v-list-item-group>

    <product-details :drawer="productDetailsDrawer" />
  </v-list>
</template>

<script>
import ProductItem from '@/components/ProductItem'
import ProductDetails from '@/components/ProductDetails'
export default {
  components: {
    ProductItem,
    ProductDetails
  },
  data: () => ({
    productDetailsDrawer: false,
    selected: [2],
    items: [
      {
        action: '15 min',
        headline: 'Brunch this weekend?',
        subtitle:
          'll be in your neighborhood doing errands this weekend. Do you want to hang out?',
        title: 'Ali Connors'
      },
      {
        action: '2 hr',
        headline: 'Summer BBQ',
        subtitle:
          'll be in your neighborhood doing errands this weekend. Do you want to hang out?',
        title: 'me, Scrott, Jennifer'
      },
      {
        action: '6 hr',
        headline: 'Oui oui',
        subtitle: 'Do you have Paris recommendations? Have you ever been?',
        title: 'Sandra Adams'
      },
      {
        action: '12 hr',
        headline: 'Birthday gift',
        subtitle:
          'Have any ideas about what we should get Heidi for her birthday?',
        title: 'Trevor Hansen'
      },
      {
        action: '18hr',
        headline: 'Recipe to try',
        subtitle:
          'We should eat this: Grate, Squash, Corn, and tomatillo Tacos.',
        title: 'Britta Holt'
      }
    ]
  })
}
</script>
