<template>
  <div id="app">
    <!-- <NumericInput :value="value" @onincrease="increaseValue" @ondecrease="decreaseValue"/> this is not optimal -->
    <!-- bananas= $event : event is the second parameter in the emit , aka new value/quantity -->
    bananas <NumericInput :value="bananas" :minimum="1" :maximum="5" @onchange="bananas = $event"/> 
    apples <NumericInput :value="apples" :minimum="2" :maximum="5" @onchange="apples =$event"/>
    lemons <NumericInput :value="lemons" :minimum="4"  :maximum="10" @onchange="lemons =$event"/> 
    pineapples <NumericInput :value="pineapples" :minimum="1" :maximum="8" @onchange="pineapples =$event"/> 
  </div>
</template>

<script>
import NumericInput from './components/NumericInput.vue'

export default {
  name: 'App',
  components: {
    NumericInput
  },
  data(){
    return {
      bananas:1,
      apples:2,
      lemons:4,
      pineapples:1
      // value:1
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
