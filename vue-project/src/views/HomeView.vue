<template>
  <div>
    <CpuSelector @cpu-selected="updateTotalPrice" />
    <GpuCard @gpu-selected="updateTotalPrice" />
    <!-- <MotherboardSelector />
    <RamSelector /> -->

    <TotalPrice :total="totalPrice" />
  </div>  
</template>

<script>
import { ref } from 'vue';
import CpuSelector from '@/components/cpuSelector.vue';
import GpuCard from '@/components/gpuCard.vue';
import TotalPrice from '@/components/totalPrice.vue';


export default {
  components: {
    CpuSelector,
    GpuCard,
    TotalPrice
},
  setup() {
    const totalPrice = ref(0);

    const updateTotalPrice = (price) => {
      totalPrice.value + price;
    };

    return { totalPrice, updateTotalPrice };
  }
}
</script>

<style scoped>


</style>
