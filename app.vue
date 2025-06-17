<template>
  <div class="container">
    <h1>Compute Product</h1>
    <img src="https://www.rd.com/wp-content/uploads/2022/04/GettyImages-1140602972-e1748616001999.jpg?fit=300,300&webp=1" alt="Airplane wing" class="plane-image" />
    
    <p>Number 1: {{ num1 }}</p>
    <p>Number 2: {{ num2 }}</p>

    <button v-if="!computed" @click="computeProduct">Compute</button>

    <p v-else>Product: {{ product }}</p>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const num1 = ref(4)
const num2 = ref(8)
const product = ref(0)
const computed = ref(false)

function computeProduct() {
  product.value = num1.value * num2.value
  computed.value = true
}
</script>

<style scoped>
.container {
  text-align: center;
  padding: 20px;
}
h1 {
  color: darkblue;
}

.plane-image {
  width: 360px;
  height: auto;
  margin: 20px auto;
  display: block;
  border-radius: 8px;
}

button {
  margin-top: 20px;
  background-color: green;
  padding: 10px 10px;
  font-size: 20px;
  border-radius: 5px;
  border-color: white;
  cursor: pointer;
}

p {
  font-size: 18px;
}

button:hover {
  background-color: darkgreen;
}
</style>