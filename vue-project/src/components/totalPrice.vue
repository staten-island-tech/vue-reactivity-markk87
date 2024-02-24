<template>
    <div>
      <h2>Total Price: ${{ totalPrice }}</h2>
    </div>
  </template>
  
  <script setup>
  import { ref, watch } from 'vue';
//   import { selectedCPU } from './cpuSelector.vue';
//   import { selectedGPU } from './gpuCard.vue';
  
//   const totalPrice = ref(0);
  
//   watch([selectedCPU, selectedGPU], ([cpu, gpu]) => {
//     if (cpu && gpu) {
//       totalPrice.value = cpu.price + gpu.price;
//     } else if (cpu) {
//       totalPrice.value = cpu.price;
//     } else if (gpu) {
//       totalPrice.value = gpu.price;
//     } else {
//       totalPrice.value = 0;
//     }
//   });
  </script>
  