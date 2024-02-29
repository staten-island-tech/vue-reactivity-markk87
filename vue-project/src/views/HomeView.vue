<template>
  <div>
    <CpuSelector />
    <GpuCard />
    <MotherboardSelector />
    <RamSelector />

    <TotalPrice />
  </div>  
</template>

<script setup>

import CpuSelector from '@/components/cpuSelector.vue';
import GpuCard from '@/components/gpuCard.vue';
import TotalPrice from '@/components/totalPrice.vue';
import MotherboardSelector from '@/components/motherboardSelector.vue';
import RamSelector from '@/components/ramSelector.vue';



</script>

<style scoped>


</style>
