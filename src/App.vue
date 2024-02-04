<script setup>

import { ref } from 'vue';

const resposta = ref(0);
const num1 = ref(0);
const num2 = ref(0);

function somarNumeros () {
  resposta.value = Number(num1.value) + Number(num2.value);
}

function subtrairNumeros () {
  resposta.value = Number(num1.value) - Number(num2.value);
}
function dividirNumeros () {
  resposta.value = Number(num1.value) / Number(num2.value);
}
function multiplicarNumeros () {
  resposta.value = Number(num1.value) * Number(num2.value);
}

</script>

<template>
  <div class="container">
    <header class="p-5 mb-4 mt-4 bg-ligth rounded-3 ">
      <h1>Calculadora</h1>
    </header>
    <input v-model="num1"  class="me-2" type="number" placeholder="Primeiro número">
    <input v-model="num2" type="number" placeholder="Segundo número">
    <br>
    <div class="operadores">
      <button v-on:click ="somarNumeros" class="btn btn-primary m-2 fw-bold ">+</button>
      <button v-on:click ="subtrairNumeros" class="btn btn-primary m-2 fw-bold" type="submit">-</button>
      <button v-on:click ="dividirNumeros" class="btn btn-primary m-2 fw-bold" type="submit">/</button>
      <button v-on:click ="multiplicarNumeros" class="btn btn-primary m-2 fw-bold" type="submit">*</button>
    </div>
    <h3>Resposta: {{ resposta }}</h3>
  </div>
</template>

<style scoped>

</style>
