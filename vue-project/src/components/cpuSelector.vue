<template>
    <div>
        <h1 class="cpuHeader">Central Processing Unit:</h1>
        <select v-model="selectedCPU" class="cpuSelector">
        <option class="cpuOption" v-for="cpu in cpus" :key="cpu.name" :value="cpu" >{{ cpu.name }} - ${{ cpu.price }}</option>
        </select>
    </div>
</template>

<script setup>
import { ref } from 'vue';
import { store } from '@/stores/store';

const selectedCPU = ref(null);

store.selectedCPU = selectedCPU;
        
const cpus = [
    {"name":"AMD Ryzen 7 7800X3D","price":369,"core_count":8,"core_clock":4.2,"boost_clock":5,"tdp":120,"graphics":"Radeon","smt":true},{"name":"AMD Ryzen 5 7600X","price":224,"core_count":6,"core_clock":4.7,"boost_clock":5.3,"tdp":105,"graphics":"Radeon","smt":true},{"name":"AMD Ryzen 5 5600X","price":154.15,"core_count":6,"core_clock":3.7,"boost_clock":4.6,"tdp":65,"graphics":null,"smt":true},{"name":"Intel Core i9-14900K","price":544.99,"core_count":24,"core_clock":3.2,"boost_clock":6,"tdp":125,"graphics":"Intel UHD Graphics 770","smt":true},{"name":"AMD Ryzen 5 7600","price":210.99,"core_count":6,"core_clock":3.8,"boost_clock":5.1,"tdp":65,"graphics":"Radeon","smt":true},{"name":"Intel Core i7-13700K","price":370.99,"core_count":16,"core_clock":3.4,"boost_clock":5.4,"tdp":125,"graphics":"Intel UHD Graphics 770","smt":true},{"name":"AMD Ryzen 5 5600","price":134.99,"core_count":6,"core_clock":3.5,"boost_clock":4.4,"tdp":65,"graphics":null,"smt":true},{"name":"Intel Core i5-12400F","price":148.99,"core_count":6,"core_clock":2.5,"boost_clock":4.4,"tdp":65,"graphics":null,"smt":true},{"name":"AMD Ryzen 7 5800X","price":219.13,"core_count":8,"core_clock":3.8,"boost_clock":4.7,"tdp":105,"graphics":null,"smt":true},{"name":"AMD Ryzen 5 5500","price":98.2,"core_count":6,"core_clock":3.6,"boost_clock":4.2,"tdp":65,"graphics":null,"smt":true},{"name":"Intel Core i7-14700K","price":399.99,"core_count":20,"core_clock":3.4,"boost_clock":5.6,"tdp":125,"graphics":"Intel UHD Graphics 770","smt":true},{"name":"AMD Ryzen 5 3600","price":109.31,"core_count":6,"core_clock":3.6,"boost_clock":4.2,"tdp":65,"graphics":null,"smt":true},{"name":"AMD Ryzen 7 7700X","price":287.99,"core_count":8,"core_clock":4.5,"boost_clock":5.4,"tdp":105,"graphics":"Radeon","smt":true},{"name":"AMD Ryzen 9 7950X3D","price":599,"core_count":16,"core_clock":4.2,"boost_clock":5.7,"tdp":120,"graphics":"Radeon","smt":true},{"name":"Intel Core i5-12600K","price":169.96,"core_count":10,"core_clock":3.7,"boost_clock":4.9,"tdp":125,"graphics":"Intel UHD Graphics 770","smt":true},{"name":"AMD Ryzen 7 5700X","price":179.61,"core_count":8,"core_clock":3.4,"boost_clock":4.6,"tdp":65,"graphics":null,"smt":true},{"name":"Intel Core i7-12700K","price":236.98,"core_count":12,"core_clock":3.6,"boost_clock":5,"tdp":125,"graphics":"Intel UHD Graphics 770","smt":true},{"name":"AMD Ryzen 7 5800X3D","price":295.58,"core_count":8,"core_clock":3.4,"boost_clock":4.5,"tdp":105,"graphics":null,"smt":true},{"name":"Intel Core i5-13600K","price":297.99,"core_count":14,"core_clock":3.5,"boost_clock":5.1,"tdp":125,"graphics":"Intel UHD Graphics 770","smt":true},{"name":"AMD Ryzen 5 5600G","price":139,"core_count":6,"core_clock":3.9,"boost_clock":4.4,"tdp":65,"graphics":"Radeon Vega 7","smt":true},{"name":"AMD Ryzen 9 7900X","price":383.23,"core_count":12,"core_clock":4.7,"boost_clock":5.6,"tdp":170,"graphics":"Radeon","smt":true},{"name":"Intel Core i5-12600KF","price":152.97,"core_count":10,"core_clock":3.7,"boost_clock":4.9,"tdp":125,"graphics":null,"smt":true},{"name":"Intel Core i3-12100F","price":96.99,"core_count":4,"core_clock":3.3,"boost_clock":4.3,"tdp":58,"graphics":null,"smt":true},{"name":"AMD Ryzen 9 5900X","price":298.99,"core_count":12,"core_clock":3.7,"boost_clock":4.8,"tdp":105,"graphics":null,"smt":true},{"name":"AMD Threadripper 3990X","price":4255,"core_count":64,"core_clock":2.9,"boost_clock":4.3,"tdp":280,"graphics":null,"smt":true},{"name":"Intel Core i7-14700KF","price":379,"core_count":20,"core_clock":3.4,"boost_clock":5.6,"tdp":125,"graphics":null,"smt":true},{"name":"Intel Core i5-13400F","price":203.99,"core_count":10,"core_clock":2.5,"boost_clock":4.6,"tdp":65,"graphics":null,"smt":true},{"name":"AMD Ryzen 5 4500","price":78.5,"core_count":6,"core_clock":3.6,"boost_clock":4.1,"tdp":65,"graphics":null,"smt":true},{"name":"Intel Core i9-13900K","price":524.99,"core_count":24,"core_clock":3,"boost_clock":5.8,"tdp":125,"graphics":"Intel UHD Graphics 770","smt":true},{"name":"Intel Core i5-14600K","price":299.99,"core_count":14,"core_clock":3.5,"boost_clock":5.3,"tdp":125,"graphics":"Intel UHD Graphics 770","smt":true},{"name":"Intel Core i9-12900K","price":324.99,"core_count":16,"core_clock":3.2,"boost_clock":5.2,"tdp":125,"graphics":"Intel UHD Graphics 770","smt":true},{"name":"AMD Ryzen 9 7950X","price":549.99,"core_count":16,"core_clock":4.5,"boost_clock":5.7,"tdp":170,"graphics":"Radeon","smt":true}
];


</script>

<style scoped>

.cpuSelector:hover {
    transform: scale(1.15);
    transition: all 0.5s ease-out;
}

.cpuHeader {
    font-size: 1.4rem;
    color: white;
    font-family: 'Times New Roman', Times, serif;
}

</style>
