<template>
  <div>
    <ul class="product-list">
      <item v-for="item in items" :item="item"></item>
    </ul>
  </div>
</template>

<script>
import Item from './Item.vue'

export default {
  props: ['items'],
  name: 'item-list',
  components: {
    Item
  },
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .product-list {
    margin: 0;
    padding: 0;
  }
</style>
