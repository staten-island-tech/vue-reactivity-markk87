<template>
  <div>
    <CpuSelector />
    <GpuCard />
    <MotherboardSelector />
    <RamSelector />
    <SsdSelector />


    <h2 class="totalPrice">Total Price:</h2>
    <TotalPrice />
  </div>  
</template>

<script setup>

import CpuSelector from '@/components/cpuSelector.vue';
import GpuCard from '@/components/gpuCard.vue';
import TotalPrice from '@/components/totalPrice.vue';
import MotherboardSelector from '@/components/motherboardSelector.vue';
import RamSelector from '@/components/ramSelector.vue';
import SsdSelector from '@/components/ssdSelector.vue';



</script>

<style scoped>

.totalPrice {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
}

</style>
