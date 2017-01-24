<template>
  <div class="container">
    <div class="row">
      <ul class="costumer-details col-xs-12">
        <li class="costumer-details__item">Aangevraagd om: <span>09.00 (24-05-2016)</span></li>
        <li class="costumer-details__item">Email: <span>email@email.nl</span></li>
        <li class="costumer-details__item">Telefoon: <span>04647383929</span></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'costumer-details',
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  .costumer-details { 
    margin: 0;
    padding: 15px 10px;
  }

  .costumer-details__item { 
    list-style: none; 
    font-weight: bold;
    span { font-weight: normal; }
  }
</style>
