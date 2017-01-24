<template>
  <div class="container">
    <div class="row">
      <ul class="customer-details col-xs-12">
        <li class="customer-details__item">
          Aangevraagd om: <span>{{ requestedDatetime }}</span>
        </li>
        <li class="customer-details__item">Email: <span>{{ customer.email }}</span></li>
        <li class="customer-details__item">Telefoon: <span>{{ customer.phoneNumber }}</span></li>
      </ul>
    </div>
  </div>
</template>

<script>
import moment from 'moment'

export default {
  props: ['requested', 'customer'],
  name: 'customer-details',
  computed: {
    requestedDatetime () {
      return moment(this.requested).format('HH:mm (DD-MM-YYYY)')
    }
  },
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  .customer-details { 
    margin: 0;
    padding: 15px 10px;
  }

  .customer-details__item { 
    list-style: none; 
    font-weight: bold;
    span { font-weight: normal; }
  }
</style>
