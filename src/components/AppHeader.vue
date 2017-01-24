<template>
  <div class="navigation">
    <div class="container">
      <div class="row">
        <div class="col-xs-2">
          <a href="#" class="button hidden-print">
            <span class="hidden">Back</span>
            <span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
          </a>
        </div>
        <div class="col-xs-8">
          <p class="costumer-info">
            <span class="costumer-info__name">Mevr de Boer</span>
            <small class="costumer-info__id">7487473287</small>
          </p>
        </div>
        <div class="col-xs-2">
          <a href="#" class="button button--grey pull-right hidden-print" 
            @click="printDocument()">
            <span class="hidden">Print</span>
            <span class="glyphicon glyphicon-print" aria-hidden="true"></span>
          </a>     
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app-header',
  data () {
    return {
    }
  },
  methods: {
    printDocument () {
      window.print()
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  .navigation {
    padding-top: 5px;
    padding-bottom: 5px;
    border-bottom: 1px solid #f0f0f0;
  }

  .button { 
    color: #737373;
    padding: 10px;
    font-size: 1.2em;
    display: block;
    width: 40px;
    height: 40px;
    text-align: center;
  }
  
  .button--grey {
    color: #fff;
    background: #737373;  
  }

  .costumer-info {
    text-align: center;
    margin: 0;
  }
  .costumer-info__name {
    display: block;
    width: 100%;
    font-weight: bold;
    font-size: 1.1em;
  }

  .costumer-info__id {
    color: #a2a2a2;
  }

</style>
