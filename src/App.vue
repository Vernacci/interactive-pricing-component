<script setup>
import Pricing from './components/Pricing.vue';
</script>

<template>
  <Pricing />
</template>

<style>
:root {
  --dark-blue: hsl(227, 35%, 25%);
  --gray-blue: hsl(225, 20%, 60%);
  --bg-white: hsl(230, 100%, 99%);
}

#app {
  background-color: var(--bg-white);
  font-family: 'Manrope', sans-serif;
}
</style>
