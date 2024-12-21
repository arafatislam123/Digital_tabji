<script setup>
import { ref } from 'vue';
const products = ref([]);

CallApi();
async function CallApi() {
  const response = await fetch('https://dummyjson.com/products');
  const data = await response.json();
  products.value = data.products; // Access the products array
  console.log(data);
}
</script>

<template>
  <table>
    <thead>
    <tr>
      <th>Id</th>
      <th>Name</th>
      <th>Price</th>
      <th>Category</th>
    </tr>
    </thead>
    <tbody>
    <tr v-for="product in products" :key="product.id">
      <td>{{ product.id }}</td>
      <td>{{ product.title }}</td>
      <td>{{ product.price }}</td>
      <td>{{ product.category }}</td>
    </tr>
    </tbody>
  </table>
</template>

<style scoped>
</style>