<template>
    <div>
        <h1 class="motherboardHeader">Motherboard:</h1>
        <select v-model="selectedMotherboard" class="mthrbrdSelect">
        <option v-for="motherboard in motherboards" :key="motherboard.name" :value="motherboard"> {{ motherboard.name }} - ${{ motherboard.price }}</option>
        </select>
    </div>
</template>

<script setup>
import { ref } from 'vue'
import { store } from '@/stores/store';

const selectedMotherboard = ref(null);

store.selectedMotherboard = selectedMotherboard;

const motherboards = [
    {"name":"Asus ROG STRIX B650-A GAMING WIFI","price":229.99,"socket":"AM5","form_factor":"ATX","max_memory":192,"memory_slots":4,"color":"Black / Silver"},{"name":"MSI B650 GAMING PLUS WIFI","price":179.99,"socket":"AM5","form_factor":"ATX","max_memory":192,"memory_slots":4,"color":"Black"},{"name":"MSI B760 GAMING PLUS WIFI","price":159.99,"socket":"LGA1700","form_factor":"ATX","max_memory":192,"memory_slots":4,"color":"Black / Silver"},{"name":"MSI B550 GAMING GEN3","price":109.99,"socket":"AM4","form_factor":"ATX","max_memory":128,"memory_slots":4,"color":"Black"},{"name":"MSI PRO Z790-A MAX WIFI","price":256.99,"socket":"LGA1700","form_factor":"ATX","max_memory":192,"memory_slots":4,"color":"Silver / Black"},{"name":"Gigabyte B650 GAMING X AX","price":189.99,"socket":"AM5","form_factor":"ATX","max_memory":192,"memory_slots":4,"color":"Black / Gray"},{"name":"Gigabyte B550M K","price":84.99,"socket":"AM4","form_factor":"Micro ATX","max_memory":128,"memory_slots":4,"color":"Brown / Silver"},{"name":"Asus ROG STRIX B550-F GAMING WIFI II","price":189.99,"socket":"AM4","form_factor":"ATX","max_memory":128,"memory_slots":4,"color":"Black / Red"},{"name":"Gigabyte B650 AORUS ELITE AX","price":199.99,"socket":"AM5","form_factor":"ATX","max_memory":192,"memory_slots":4,"color":"Black / Silver"},{"name":"ASRock B660M Pro RS","price":94.99,"socket":"LGA1700","form_factor":"Micro ATX","max_memory":128,"memory_slots":4,"color":"Gray / Black"},{"name":"MSI MAG B650 TOMAHAWK WIFI","price":212.71,"socket":"AM5","form_factor":"ATX","max_memory":192,"memory_slots":4,"color":"Black"},{"name":"Asus PRIME B550M-A WIFI II","price":129.99,"socket":"AM4","form_factor":"Micro ATX","max_memory":128,"memory_slots":4,"color":"Blue / Silver"},{"name":"MSI PRO B650M-A WIFI","price":149.99,"socket":"AM5","form_factor":"Micro ATX","max_memory":192,"memory_slots":4,"color":"Black"},{"name":"ASRock B650M Pro RS","price":129.99,"socket":"AM5","form_factor":"Micro ATX","max_memory":192,"memory_slots":4,"color":"Black / Silver"},{"name":"ASRock B650M Pro RS WiFi","price":149.99,"socket":"AM5","form_factor":"Micro ATX","max_memory":192,"memory_slots":4,"color":"Black / Silver"},{"name":"MSI B450M-A PRO MAX II","price":69.98,"socket":"AM4","form_factor":"Micro ATX","max_memory":64,"memory_slots":2,"color":"Black"},{"name":"Gigabyte Z790 AORUS ELITE AX","price":229.99,"socket":"LGA1700","form_factor":"ATX","max_memory":192,"memory_slots":4,"color":"Black"},{"name":"MSI MAG B550 TOMAHAWK MAX WIFI","price":159.99,"socket":"AM4","form_factor":"ATX","max_memory":128,"memory_slots":4,"color":"Silver / Black"},{"name":"MSI PRO B550M-VC WIFI","price":117.56,"socket":"AM4","form_factor":"Micro ATX","max_memory":128,"memory_slots":4,"color":"Black"},{"name":"MSI MAG Z790 TOMAHAWK WIFI","price":239.99,"socket":"LGA1700","form_factor":"ATX","max_memory":192,"memory_slots":4,"color":"Black"},{"name":"Asus ROG MAXIMUS Z790 DARK HERO","price":649.99,"socket":"LGA1700","form_factor":"ATX","max_memory":192,"memory_slots":4,"color":"Black"},{"name":"Asus ROG STRIX B650E-F GAMING WIFI","price":251.7,"socket":"AM5","form_factor":"ATX","max_memory":192,"memory_slots":4,"color":"Black"},{"name":"Asus ROG ZENITH II EXTREME ALPHA","price":2059,"socket":"sTRX4","form_factor":"EATX","max_memory":256,"memory_slots":8,"color":"Black / Silver"},{"name":"MSI PRO B760-P WIFI DDR4","price":159.99,"socket":"LGA1700","form_factor":"ATX","max_memory":128,"memory_slots":4,"color":"Black"},{"name":"MSI MAG X670E TOMAHAWK WIFI","price":279.99,"socket":"AM5","form_factor":"ATX","max_memory":192,"memory_slots":4,"color":"Black"},{"name":"MSI PRO Z790-P WIFI","price":189.99,"socket":"LGA1700","form_factor":"ATX","max_memory":192,"memory_slots":4,"color":"Black / Silver"},{"name":"Asus TUF GAMING B550-PLUS WIFI II","price":159.99,"socket":"AM4","form_factor":"ATX","max_memory":128,"memory_slots":4,"color":"Black / Gray"},{"name":"MSI B550-A PRO","price":109.99,"socket":"AM4","form_factor":"ATX","max_memory":128,"memory_slots":4,"color":"Black / Silver"},{"name":"Asus ROG STRIX Z790-A GAMING WIFI II","price":359.99,"socket":"LGA1700","form_factor":"ATX","max_memory":192,"memory_slots":4,"color":"Black / Silver"},{"name":"MSI PRO B650M-P","price":119.99,"socket":"AM5","form_factor":"Micro ATX","max_memory":192,"memory_slots":4,"color":"Black / Silver"},{"name":"MSI B550M PRO-VDH WIFI","price":119.99,"socket":"AM4","form_factor":"Micro ATX","max_memory":128,"memory_slots":4,"color":"Black"},{"name":"Gigabyte B650 AORUS ELITE AX ICE","price":219.99,"socket":"AM5","form_factor":"ATX","max_memory":192,"memory_slots":4,"color":"Silver"},{"name":"Asus TUF GAMING B650-PLUS WIFI","price":199.99,"socket":"AM5","form_factor":"ATX","max_memory":128,"memory_slots":4,"color":"Black"},{"name":"ASRock A620M Pro RS WiFi","price":129.99,"socket":"AM5","form_factor":"Micro ATX","max_memory":192,"memory_slots":4,"color":"Silver / Black"},{"name":"Gigabyte X670E AORUS PRO X","price":299.99,"socket":"AM5","form_factor":"ATX","max_memory":192,"memory_slots":4,"color":"White / Silver"},{"name":"Asus ROG STRIX B760-I GAMING WIFI","price":207.01,"socket":"LGA1700","form_factor":"Mini ITX","max_memory":96,"memory_slots":2,"color":"Black"},{"name":"Asus ROG STRIX Z790-E GAMING WIFI II","price":449.99,"socket":"LGA1700","form_factor":"ATX","max_memory":192,"memory_slots":4,"color":"Black"},{"name":"ASRock B550M Pro4","price":106.49,"socket":"AM4","form_factor":"Micro ATX","max_memory":128,"memory_slots":4,"color":"Silver / Black"},{"name":"MSI B450M PRO-VDH MAX","price":74.98,"socket":"AM4","form_factor":"Micro ATX","max_memory":64,"memory_slots":4,"color":"Black / Silver"},{"name":"Asus Prime B450M-A II","price":79.98,"socket":"AM4","form_factor":"Micro ATX","max_memory":128,"memory_slots":4,"color":null},{"name":"MSI PRO H610M-G DDR4","price":86.33,"socket":"LGA1700","form_factor":"Micro ATX","max_memory":64,"memory_slots":2,"color":"Black / Silver"},{"name":"Asus ROG STRIX B550-A GAMING","price":169,"socket":"AM4","form_factor":"ATX","max_memory":128,"memory_slots":4,"color":"Black / White"},{"name":"Gigabyte B650I AORUS ULTRA","price":337.88,"socket":"AM5","form_factor":"Mini ITX","max_memory":96,"memory_slots":2,"color":"Black / Silver"},{"name":"Asus TUF GAMING Z790-PLUS WIFI","price":218,"socket":"LGA1700","form_factor":"ATX","max_memory":192,"memory_slots":4,"color":"Black / Gray"},{"name":"Asus ROG STRIX B650E-I GAMING WIFI","price":311.99,"socket":"AM5","form_factor":"Mini ITX","max_memory":96,"memory_slots":2,"color":"Black"}
]



</script>

<style scoped>

.mthrbrdSelect:hover {
    transform: scale(1.15);
    transition: all 0.5s ease-out;
}

.motherboardHeader {
    font-size: 1.4rem;
    color: white;
    font-family: 'Times New Roman', Times, serif;
}

</style>