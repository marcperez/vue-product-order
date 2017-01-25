<template>
  <li class="row product">
    <div class="col-xs-2">
      <checkbox :value="item.status" true-value="RESERVED" false-value="NEW"
        @input="updateItemStatus"></checkbox>
    </div>
    <div class="col-xs-3 product__image">
      <img :src="item.product.imageUrl" alt="">
    </div>
    <div class="col-xs-7">
      <h2 class="product__title">{{ item.product.name }}</h2>
      <p class="product__description">{{ item.product.description }}</p>
    </div>
    <div class="product__chevron">
      <span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
    </div>
  </li>    
</template>

<script>
import Checkbox from './Checkbox.vue'
export default {
  props: ['item'],
  name: 'item',
  data () {
    return {
    }
  },
  methods: {
    updateItemStatus (newStatus) {
      this.item.status = newStatus
    }
  },
  components: {
    Checkbox
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .product { 
    position: relative;
    list-style: none; 
    padding: 20px 0;
    margin: 0 10px;
    border-bottom: 1px solid #efefef;
  }

  .product__title {
    font-size: 1em;
    margin: 0;
    font-weight: bold;
    text-transform: uppercase;
  }

  .product__description {
    overflow: hidden;
    text-overflow: ellipsis;
    word-wrap: break-word;
    line-height: 19px;
    max-height: 38px;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
  }

  .product__chevron {
    position: absolute;
    right: 0;
    top: 50%;
    margin-top: -7.5px;
    color: #acacac;
    font-size: 11px;
  }
</style>
