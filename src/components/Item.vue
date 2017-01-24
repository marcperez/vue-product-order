<template>
  <li class="row product">
    <div class="col-xs-2">
      <checkbox></checkbox>
    </div>
    <div class="col-xs-3 product__image">
      <img src="//placehold.it/57/ffffff/000000" alt="">
    </div>
    <div class="col-xs-7">
      <h2 class="product__title">Item</h2>
      <p class="product__description">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sapiente, quod.</p>
    </div>
  </li>    
</template>

<script>
import Checkbox from './Checkbox.vue'
export default {
  name: 'item',
  data () {
    return {
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
    list-style: none; 
    padding: 20px 0;
    margin: 0 10px;
    border-bottom: 1px solid #efefef;
  }

  .product__title {
    font-size: 1.2em;
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
</style>
