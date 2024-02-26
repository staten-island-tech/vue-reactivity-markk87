<script setup>
import { RouterLink, RouterView } from 'vue-router'


</script>

<template>
  <header>
    

    <div class="wrapper">
      
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>

header {
  line-height: 1.5;
  max-height: 100vh;
  width: 100%; 
  display: flex;
  justify-content: center; 
  align-items: center; 
 
}

.wrapper {
  width: 100%;
  color: blue;
}

nav {
  font-size: 5rem;
  font-family: 'Times New Roman', Times, serif;
  text-align: center;
  margin-top: 0.2rem;
}

nav a.router-link-exact-active {
  color: green;
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}
</style>
