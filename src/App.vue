<template>
  <div id="app">
    <app-header :customer="order.customer"></app-header>
    <customer-details :requested="order.placedAt" :customer="order.customer"></customer-details>
    <status-details :status="order.status" :assignee="order.assignee" 
      :assignedAt="order.assignedAt"></status-details>
    <item-list :items="order.items"></item-list>
  </div>
</template>

<script>
import postData from './data/data.json'
import AppHeader from './components/AppHeader.vue'
import CustomerDetails from './components/CustomerDetails.vue'
import StatusDetails from './components/StatusDetails.vue'
import ItemList from './components/ItemList.vue'

export default {
  name: 'app',
  data () {
    return {
      order: postData.data
    }
  },
  components: {
    AppHeader,
    CustomerDetails,
    StatusDetails,
    ItemList
  }
}
</script>

<style lang="scss">
  $icon-font-path: "~bootstrap-sass/assets/fonts/bootstrap/";
  @import "~bootstrap-sass/assets/stylesheets/bootstrap";
</style>
