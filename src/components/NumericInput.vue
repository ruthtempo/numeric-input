<template>
  <div>
    <button @click="increase">+</button>
    {{value}}
    <button @click="decrease">-</button>
  </div>
</template>

<script>
export default {
  name: 'NumericInput',
  props:{
    value: Number,
    minimum : Number,
    maximum: Number
  },
  methods:{
    increase(){
      this.$emit("onchange", this.value < this.maximum ? this.value +1: this.value)
    }, 
    decrease(){
      this.$emit("onchange", this.value > this.minimum? this.value -1: this.value)
      // mutations: +=, =, *=, ++, --, /=
      // statements: *, +, -,  / they dont mutate
    }
  },
  emits:['onchange'],
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
