<template>
    <div>
    <button @click="calculateTotalPrice">Calculate Total Price</button>
    <h1 class="totalHeader">${{ totalPrice }}</h1>
    </div>
  </template>
  
<script setup>
import { ref } from 'vue';
import { store } from '@/stores/store';

const totalPrice = ref(0);

function calculateTotalPrice() {
  let selectedParts = [store.selectedCPU, store.selectedGPU, store.selectedRAM, store.selectedMotherboard, store.selectedSSD];
  totalPrice.value = selectedParts.reduce((acc, part) => acc + (part ? part.price : 0), 0);
}
  </script>
  
  <style scoped>
.totalHeader {
    font-size: 1.4rem;
    color: white;
    font-family: 'Times New Roman', Times, serif;
}

  </style>
  