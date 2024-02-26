<template>
    <div>
      <h1>Total Price:</h1>
      <p v-if="totalPrice">Combined Price: ${{ totalPrice }}</p>
      <p v-else>Please select a CPU and GPU</p>
    </div>
  </template>
  
  <script setup>
  import { ref, watch } from 'vue'
  
  const selectedCPU = ref(null);
  const selectedGPU = ref(null);
  const totalPrice = ref(0);
  
  watch([selectedCPU, selectedGPU], () => {
    if (selectedCPU.value && selectedGPU.value) {
      totalPrice.value = selectedCPU.value.price + selectedGPU.value.price;
    } else {
      totalPrice.value = 0;
    }
  });
  
  </script>
  
  <style scoped>
  
  </style>
  