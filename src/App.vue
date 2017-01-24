<template>
  <div id="app">
    <app-header></app-header>
    <costumer-details></costumer-details>
    <status-details></status-details>
    <item-list></item-list>
  </div>
</template>

<script>
import postData from './data/data.json'
import AppHeader from './components/AppHeader.vue'
import CostumerDetails from './components/CostumerDetails.vue'
import StatusDetails from './components/StatusDetails.vue'
import ItemList from './components/ItemList.vue'

export default {
  name: 'app',
  data () {
    return {
      postData: postData.data
    }
  },
  components: {
    AppHeader,
    CostumerDetails,
    StatusDetails,
    ItemList
  }
}
</script>

<style lang="scss">
  $icon-font-path: "~bootstrap-sass/assets/fonts/bootstrap/";
  @import "~bootstrap-sass/assets/stylesheets/bootstrap";
</style>
