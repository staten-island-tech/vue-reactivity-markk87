<template>
  <div>
    <h1 class="gpuHeader">Graphics Card:</h1>
    <select class="gpuSelect" v-model="selectedGPU">
      <option v-for="gpu in gpus" :key="gpu.name" :value="gpu">{{ gpu.name }} - ${{ gpu.price }}</option>
    </select>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import { store } from '@/stores/store';

const selectedGPU = ref(null);

store.selectedGPU = selectedGPU;

const gpus = [
    {"name":"MSI GeForce RTX 3060 Ventus 2X 12G","price":289.39,"chipset":"GeForce RTX 3060 12GB","memory":12,"core_clock":1320,"boost_clock":1777,"color":"Black","length":235},{"name":"Gigabyte WINDFORCE OC","price":549.99,"chipset":"GeForce RTX 4070","memory":12,"core_clock":1920,"boost_clock":2490,"color":"Black","length":261},{"name":"ASRock Radeon RX6700XT CLD 12G","price":375.99,"chipset":"Radeon RX 6700 XT","memory":12,"core_clock":2321,"boost_clock":2581,"color":"Black","length":269},{"name":"Asus DUAL OC","price":309.99,"chipset":"GeForce RTX 4060","memory":8,"core_clock":1830,"boost_clock":2535,"color":"Black","length":227},{"name":"Asus ROG STRIX GAMING OC","price":2313.98,"chipset":"GeForce RTX 4090","memory":24,"core_clock":2235,"boost_clock":2640,"color":"Black","length":358},{"name":"Gigabyte EAGLE","price":389.99,"chipset":"GeForce RTX 4060 Ti","memory":8,"core_clock":2310,"boost_clock":null,"color":"Black","length":272},{"name":"ASRock Challenger D","price":209.99,"chipset":"Radeon RX 6600","memory":8,"core_clock":1626,"boost_clock":null,"color":"Black","length":269},{"name":"Asus TUF GAMING OC","price":849,"chipset":"GeForce RTX 4070 Ti","memory":12,"core_clock":2310,"boost_clock":2760,"color":"Black","length":305},{"name":"Gigabyte GAMING OC","price":499.99,"chipset":"Radeon RX 7800 XT","memory":16,"core_clock":1295,"boost_clock":2565,"color":"Black","length":302},{"name":"PNY VCNRTX6000ADA-PB","price":9999,"chipset":"RTX 6000 Ada Generation","memory":48,"core_clock":915,"boost_clock":2505,"color":"Black / Gold","length":267},{"name":"Asus DUAL OC","price":589.99,"chipset":"GeForce RTX 4070","memory":12,"core_clock":2520,"boost_clock":2550,"color":"White","length":267},{"name":"MSI VENTUS 2X BLACK OC","price":294.99,"chipset":"GeForce RTX 4060","memory":8,"core_clock":1830,"boost_clock":2505,"color":"Black","length":199},{"name":"Sapphire PULSE","price":519.99,"chipset":"Radeon RX 7800 XT","memory":16,"core_clock":1295,"boost_clock":null,"color":"Black / Red","length":280}
  ];




</script>

<style scoped>



.gpuHeader {
  font-size: 1.4rem;
    color: white;
    font-family: 'Times New Roman', Times, serif;
}

.gpuSelect:hover {
  transform: scale(1.15);
  transition: all 0.5s ease-out;
}

</style>
