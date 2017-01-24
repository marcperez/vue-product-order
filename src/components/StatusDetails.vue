<template>
  <div class="status-details">
    <div class="container">
      <div class="row">
        <div class="col-xs-4 status-details__section">
          <strong class="status-details__header">Status</strong>
          In Behandeling
        </div>
        <div class="col-xs-3 status-details__section">
          <strong class="status-details__header">Door</strong>
          Mark
        </div>
        <div class="col-xs-5 status-details__section">
          <strong class="status-details__header">Om</strong>
          10:30 <small class="status-details__date">(25-05-2016)</small>
        </div>
      </div>  
    </div>
  </div>
</template>

<script>
export default {
  name: 'status-details',
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  .status-details {
    background: #e8e8e8;
    padding: 15px 10px;
  }
  .status-details__header {
    display: block;
    font-weight: bold;
  }
  .status-details__date {
    font-size: 0.9em;
    color: #a2a2a2;
  }
</style>
