<template>
    <div>
    <button @click="calculateTotalPrice">Calculate Total Price</button>
    <p>Total Price: ${{ totalPrice }}</p>
    </div>
  </template>
  
<script setup>
import { ref } from 'vue';
import { store } from '@/stores/store';

const totalPrice = ref(0);

function calculateTotalPrice() {
  let selectedParts = [store.selectedCPU, store.selectedGPU, store.selectedRAM, store.selectedMotherboard];
  totalPrice.value = selectedParts.reduce((acc, part) => acc + (part ? part.price : 0), 0);
}
  </script>
  
  <style scoped>
  
  </style>
  