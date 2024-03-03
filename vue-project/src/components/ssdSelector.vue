<template>
    <div>
        <h1 class="ssdHeader">SSD:</h1>
        <select v-model="selectedSSD" class="ssdSelect">
        <option v-for="ssd in SSDS" :key="ssd.name" :value="ssd"> {{ ssd.name }} - ${{ ssd.price }}</option>
        </select>
    </div>
</template>

<script setup>
import { ref } from 'vue'
import { store } from '@/stores/store';

const selectedSSD = ref(null);

store.selectedSSD = selectedSSD;


const SSDS = [{"name":"Samsung 980 Pro","price":169.99,"capacity":2000,"price_per_gb":0.085,"type":"SSD","cache":2048,"form_factor":"M.2-2280","interface":"M.2 PCIe 4.0 X4"},{"name":"Samsung 970 Evo Plus","price":91,"capacity":1000,"price_per_gb":0.091,"type":"SSD","cache":1024,"form_factor":"M.2-2280","interface":"M.2 PCIe 3.0 X4"},{"name":"Kingston NV2","price":61.7,"capacity":1000,"price_per_gb":0.062,"type":"SSD","cache":null,"form_factor":"M.2-2280","interface":"M.2 PCIe 4.0 X4"},{"name":"Samsung 980 Pro","price":89.99,"capacity":1000,"price_per_gb":0.09,"type":"SSD","cache":1024,"form_factor":"M.2-2280","interface":"M.2 PCIe 4.0 X4"},{"name":"Samsung 990 Pro","price":167.75,"capacity":2000,"price_per_gb":0.084,"type":"SSD","cache":2048,"form_factor":"M.2-2280","interface":"M.2 PCIe 4.0 X4"},{"name":"Samsung 990 Pro","price":309.99,"capacity":4000,"price_per_gb":0.077,"type":"SSD","cache":4096,"form_factor":"M.2-2280","interface":"M.2 PCIe 4.0 X4"},{"name":"Crucial P3","price":68.98,"capacity":1000,"price_per_gb":0.069,"type":"SSD","cache":null,"form_factor":"M.2-2280","interface":"M.2 PCIe 3.0 X4"},{"name":"Seagate Barracuda Compute","price":64.98,"capacity":2000,"price_per_gb":0.032,"type":7200,"cache":256,"form_factor":3.5,"interface":"SATA 6.0 Gb/s"},{"name":"Crucial P3 Plus","price":69.98,"capacity":1000,"price_per_gb":0.07,"type":"SSD","cache":null,"form_factor":"M.2-2280","interface":"M.2 PCIe 4.0 X4"},{"name":"Western Digital Black SN850X","price":158.99,"capacity":2000,"price_per_gb":0.079,"type":"SSD","cache":null,"form_factor":"M.2-2280","interface":"M.2 PCIe 4.0 X4"},{"name":"Crucial P3 Plus","price":122.28,"capacity":2000,"price_per_gb":0.061,"type":"SSD","cache":null,"form_factor":"M.2-2280","interface":"M.2 PCIe 4.0 X4"},{"name":"Western Digital Black SN770","price":74.98,"capacity":1000,"price_per_gb":0.075,"type":"SSD","cache":null,"form_factor":"M.2-2280","interface":"M.2 PCIe 4.0 X4"},{"name":"Samsung 970 Evo Plus","price":59.99,"capacity":500,"price_per_gb":0.12,"type":"SSD","cache":512,"form_factor":"M.2-2280","interface":"M.2 PCIe 3.0 X4"},{"name":"Intel 750","price":2488.87,"capacity":1200,"price_per_gb":2.074,"type":"SSD","cache":null,"form_factor":"PCIe","interface":"PCIe x4"},{"name":"Western Digital Black SN770","price":132.11,"capacity":2000,"price_per_gb":0.066,"type":"SSD","cache":null,"form_factor":"M.2-2280","interface":"M.2 PCIe 4.0 X4"},{"name":"Samsung 870 Evo","price":74.98,"capacity":1000,"price_per_gb":0.075,"type":"SSD","cache":1024,"form_factor":2.5,"interface":"SATA 6.0 Gb/s"},{"name":"Western Digital Black SN850X","price":84.99,"capacity":1000,"price_per_gb":0.085,"type":"SSD","cache":null,"form_factor":"M.2-2280","interface":"M.2 PCIe 4.0 X4"},{"name":"TEAMGROUP MP33","price":61.99,"capacity":1000,"price_per_gb":0.062,"type":"SSD","cache":null,"form_factor":"M.2-2280","interface":"M.2 PCIe 3.0 X4"},{"name":"Kingston NV2","price":114.9,"capacity":2000,"price_per_gb":0.057,"type":"SSD","cache":null,"form_factor":"M.2-2280","interface":"M.2 PCIe 4.0 X4"},{"name":"Samsung 990 Pro","price":109.99,"capacity":1000,"price_per_gb":0.11,"type":"SSD","cache":1024,"form_factor":"M.2-2280","interface":"M.2 PCIe 4.0 X4"},{"name":"Seagate BarraCuda","price":84.99,"capacity":4000,"price_per_gb":0.021,"type":5400,"cache":256,"form_factor":3.5,"interface":"SATA 6.0 Gb/s"},{"name":"Crucial P3","price":44.99,"capacity":500,"price_per_gb":0.09,"type":"SSD","cache":null,"form_factor":"M.2-2280","interface":"M.2 PCIe 3.0 X4"},{"name":"Western Digital Blue SN580","price":69,"capacity":1000,"price_per_gb":0.069,"type":"SSD","cache":null,"form_factor":"M.2-2280","interface":"M.2 PCIe 4.0 X4"},{"name":"Western Digital Black SN850X","price":296.02,"capacity":4000,"price_per_gb":0.074,"type":"SSD","cache":null,"form_factor":"M.2-2280","interface":"M.2 PCIe 4.0 X4"},{"name":"Sabrent Rocket 4 Plus","price":1199.99,"capacity":8000,"price_per_gb":0.15,"type":"SSD","cache":null,"form_factor":"M.2-2280","interface":"M.2 PCIe 4.0 X4"},{"name":"Mushkin Source HC","price":null,"capacity":16000,"price_per_gb":null,"type":"SSD","cache":null,"form_factor":2.5,"interface":"SATA 6.0 Gb/s"},{"name":"Crucial T700","price":499.99,"capacity":4000,"price_per_gb":0.125,"type":"SSD","cache":null,"form_factor":"M.2-2280","interface":"M.2 PCIe 5.0 X4"},{"name":"Seagate IronWolf Pro NAS","price":399.99,"capacity":22000,"price_per_gb":0.018,"type":7200,"cache":512,"form_factor":3.5,"interface":"SATA 6.0 Gb/s"},{"name":"Western Digital Caviar Blue","price":42.49,"capacity":1000,"price_per_gb":0.042,"type":7200,"cache":64,"form_factor":3.5,"interface":"SATA 6.0 Gb/s"},{"name":"Samsung 970 Evo Plus","price":159.99,"capacity":2000,"price_per_gb":0.08,"type":"SSD","cache":1024,"form_factor":"M.2-2280","interface":"M.2 PCIe 3.0 X4"},{"name":"TEAMGROUP MP33","price":38.99,"capacity":512,"price_per_gb":0.076,"type":"SSD","cache":null,"form_factor":"M.2-2280","interface":"M.2 PCIe 3.0 X4"},{"name":"Corsair MP400","price":1352.24,"capacity":8000,"price_per_gb":0.169,"type":"SSD","cache":null,"form_factor":"M.2-2280","interface":"M.2 PCIe 3.0 X4"},{"name":"Samsung 870 Evo","price":149.99,"capacity":2000,"price_per_gb":0.075,"type":"SSD","cache":2048,"form_factor":2.5,"interface":"SATA 6.0 Gb/s"},]

</script>

<style scoped>

.ssdSelect:hover {
    transform: scale(1.15);
    transition: all 0.5s ease-out;
}

.ssdHeader {
    font-size: 1.4rem;
    color: white;
    font-family: 'Times New Roman', Times, serif;
}

</style>