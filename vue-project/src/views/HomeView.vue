<template>
  <div>
    <cpuCard 
    v-for="cpu in cpuParts"
    :key="cpu.name"
    :cpu="cpu"
    />
  
  </div>
</template>

<script setup>



</script>

<style scoped>

</style>