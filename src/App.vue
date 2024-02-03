<script setup>

var resposta = new Vue({
  el: '#container',
  data: {
    resposta: 0,
    num1: 0,
    num2: 0,
  },
  methods: {
    somarNumeros: function() {
      this.resposta = num1 + num2
    },
    subtrairNumeros: function(){
      this.resposta = num1 - num2
    },
    dividirNumeros: function(){
      this.resposta = num1/num2
    },
    multiplicarNumeros: function(){
      this.resposta = num1*num2
    },
  },
})

</script>

<template>
  <div class="container">
    <header class="p-5 mb-4 mt-4 bg-ligth rounded-3 ">
      <h1>Calculadora</h1>
    </header>
    <input id="num1" value:`$(num1)` class="me-2" type="number" placeholder="Primeiro número">
    <input id="num2" value:`$(num2)` type="number" placeholder="Segundo número">
    <br>
    <div class="operadores">
      <button v-on:click ="somarNumeros" class="btn btn-primary m-2 fw-bold ">+</button>
      <button v-on:click ="subtrairNumeros" class="btn btn-primary m-2 fw-bold" type="submit">-</button>
      <button v-on:click ="dividirNumeros" class="btn btn-primary m-2 fw-bold" type="submit">/</button>
      <button v-on:click ="multiplicarNumeros" class="btn btn-primary m-2 fw-bold" type="submit">*</button>
    </div>
    <h3>Resposta: {{ resposta.value }}</h3>
  </div>
</template>

<style scoped>

</style>
