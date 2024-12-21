<script setup>
import { ref } from 'vue' 
const number = ref(100)
const increment = () => {
  number.value++
}
const decrement = () => {
  number.value--
}
const reset = () => {
  number.value = 100
}
</script>

<template>
  <div>
    <h1>{{ number }}</h1>
    <button @click="increment">Increment</button>
  </div>
  <div>
    <button @click="decrement">Minus</button>
    <button @click="reset">Reset</button>
  </div>
</template>

<style scoped>
</style>