<template>
    <div>
    <h1>Random Access Memory:</h1>
    <select class="ramSelect"><option v-for="memory in ram"
    :key="memory.name" :value="memory"> {{ memory.name }} - ${{ memory.price }}</option>
    </select>
    </div>
</template>

<script setup>
import { ref } from 'vue';
import { store } from '@/stores/store';

const selectedRAM = ref(null);

store.selectedRAM = selectedRAM;

const ram = [{"name":"Corsair Vengeance LPX 16 GB","price":43.99,"speed":[4,3200],"modules":[2,8],"price_per_gb":2.749,"color":"Black / Yellow","first_word_latency":10,"cas_latency":16},{"name":"Corsair Vengeance 32 GB","price":109.99,"speed":[5,5600],"modules":[2,16],"price_per_gb":3.437,"color":"Black","first_word_latency":12.857,"cas_latency":36},{"name":"G.Skill Trident Z5 RGB 32 GB","price":117.99,"speed":[5,6000],"modules":[2,16],"price_per_gb":3.687,"color":"Black","first_word_latency":12,"cas_latency":36},{"name":"Corsair Vengeance RGB Pro 32 GB","price":99.99,"speed":[4,3600],"modules":[2,16],"price_per_gb":3.125,"color":"Black","first_word_latency":10,"cas_latency":18},{"name":"G.Skill Trident Z5 RGB 64 GB","price":217.99,"speed":[5,6400],"modules":[2,32],"price_per_gb":3.406,"color":"Black / Silver","first_word_latency":10,"cas_latency":32},{"name":"G.Skill Flare X5 32 GB","price":106.66,"speed":[5,6000],"modules":[2,16],"price_per_gb":3.333,"color":"Black","first_word_latency":12,"cas_latency":36},{"name":"Corsair Vengeance LPX 32 GB","price":81.99,"speed":[4,3600],"modules":[2,16],"price_per_gb":2.562,"color":"Black / Yellow","first_word_latency":10,"cas_latency":18},{"name":"Corsair Vengeance RGB 32 GB","price":127.99,"speed":[5,6000],"modules":[2,16],"price_per_gb":4,"color":"White","first_word_latency":12,"cas_latency":36},{"name":"TEAMGROUP T-Force Delta RGB 32 GB","price":109.99,"speed":[5,6000],"modules":[2,16],"price_per_gb":3.437,"color":"White","first_word_latency":10,"cas_latency":30},{"name":"Corsair Vengeance RGB Pro 16 GB","price":55.99,"speed":[4,3200],"modules":[2,8],"price_per_gb":3.499,"color":"Black","first_word_latency":10,"cas_latency":16},{"name":"Corsair Vengeance 32 GB","price":127.99,"speed":[5,6000],"modules":[2,16],"price_per_gb":4,"color":"Black / Gray","first_word_latency":10,"cas_latency":30},{"name":"Corsair Vengeance RGB 32 GB","price":119.99,"speed":[5,6000],"modules":[2,16],"price_per_gb":3.75,"color":"Black","first_word_latency":13.333,"cas_latency":40},{"name":"TEAMGROUP T-Force Delta RGB 32 GB","price":109.99,"speed":[5,6000],"modules":[2,16],"price_per_gb":3.437,"color":"Black","first_word_latency":10,"cas_latency":30},{"name":"Corsair Vengeance 16 GB","price":69.98,"speed":[5,5200],"modules":[2,8],"price_per_gb":4.374,"color":"Black","first_word_latency":15.385,"cas_latency":40},{"name":"Corsair Dominator Platinum 32 GB","price":1674.47,"speed":[4,2666],"modules":[4,8],"price_per_gb":52.327,"color":"Black / Silver","first_word_latency":11.253,"cas_latency":15},{"name":"Corsair Vengeance LPX 16 GB","price":43.99,"speed":[4,3600],"modules":[2,8],"price_per_gb":2.749,"color":"Black","first_word_latency":10,"cas_latency":18},{"name":"G.Skill Ripjaws V 32 GB","price":69.98,"speed":[4,3200],"modules":[2,16],"price_per_gb":2.187,"color":"Black","first_word_latency":10,"cas_latency":16},{"name":"Silicon Power GAMING 16 GB","price":35.97,"speed":[4,3200],"modules":[2,8],"price_per_gb":2.248,"color":"Black / Gray","first_word_latency":10,"cas_latency":16},{"name":"G.Skill Ripjaws S5 32 GB","price":114.99,"speed":[5,6000],"modules":[2,16],"price_per_gb":3.593,"color":"Black","first_word_latency":10,"cas_latency":30},{"name":"Corsair Vengeance 64 GB","price":169.99,"speed":[5,5200],"modules":[2,32],"price_per_gb":2.656,"color":"Black","first_word_latency":15.385,"cas_latency":40},{"name":"G.Skill Trident Z5 Neo RGB 32 GB","price":117.99,"speed":[5,6000],"modules":[2,16],"price_per_gb":3.687,"color":"Black","first_word_latency":10,"cas_latency":30},{"name":"Corsair Vengeance RGB Pro SL 32 GB","price":94.99,"speed":[4,3600],"modules":[2,16],"price_per_gb":2.968,"color":"White / Black","first_word_latency":10,"cas_latency":18},{"name":"Corsair Vengeance RGB 32 GB","price":117.99,"speed":[5,6000],"modules":[2,16],"price_per_gb":3.687,"color":"Black","first_word_latency":12,"cas_latency":36},{"name":"Corsair Vengeance LPX 32 GB","price":76.98,"speed":[4,3200],"modules":[2,16],"price_per_gb":2.406,"color":"Black / Yellow","first_word_latency":10,"cas_latency":16},{"name":"G.Skill Flare X5 32 GB","price":106.99,"speed":[5,6000],"modules":[2,16],"price_per_gb":3.343,"color":"Black","first_word_latency":10,"cas_latency":30}]

</script>



<style lang="scss" scoped>

</style>