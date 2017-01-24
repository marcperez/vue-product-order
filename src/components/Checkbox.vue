<template>
    <div class="checkbox">
        <input type="checkbox" class="checkbox__input" :id="'checkbox-' + _uid" 
          true-value="RESERVED" false-value="NEW" v-model="toggle">
        <label class="checkbox__label" :for="'checkbox-' + _uid">
          <slot></slot>
        </label>
    </div>
</template>

<script>
export default {
  props: {
    value: null,
    trueValue: {
      type: String,
      default: 'true'
    },
    falseValue: {
      type: String,
      default: 'false'
    }
  },
  name: 'checkbox',
  data () {
    return {
      toggle: this.value
    }
  },
  watch: {
    toggle (newVal) {
      this.$emit('input', newVal)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.checkbox__label {
  position: relative;
  padding-left: 35px;
  cursor: pointer;
  display: inline-block;
  height: 30px;
  line-height: 30px;
  font-size: 1rem;
  -webkit-user-select: none;
  -moz-user-select: none;
  -khtml-user-select: none;
  -ms-user-select: none;
}

.checkbox__label:before, .checkbox__label:after {
  content: '';
  left: 0;
  position: absolute;
  transition: border .25s, background-color .25s, width .20s .1s, height .20s .1s, top .20s .1s, left .20s .1s;
  z-index: 1;
}

.checkbox__input:checked+.checkbox__label:after {
  top: 0;
  width: 30px;
  height: 30px;
  border: 2px solid #f29908;
  background-color: #f29908;
  z-index: 0;
}

.checkbox__input:checked+.checkbox__label:before {
  top: 4px;
  left: 4px;
  width: 9px;
  height: 18px;
  border-top: 2px solid transparent;
  border-left: 2px solid transparent;
  border-right: 2px solid #fff;
  border-bottom: 2px solid #fff;
  -webkit-transform: rotate(40deg);
  transform: rotate(40deg);
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
  -webkit-transform-origin: 100% 100%;
  transform-origin: 100% 100%;
  z-index: 1;
}

.checkbox__label:before, .checkbox__label:after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 30px;
  height: 30px;
  z-index: 0;
  border: 2px solid #5a5a5a;
  border-radius: 1px;
  margin-top: 2px;
  transition: .2s;
}

.checkbox__input {
  visibility: hidden;
}
</style>
