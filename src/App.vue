<script setup>
import Header from './components/Header.vue';
import Slider from './components/Slider.vue';
</script>

<template>
  <Header />
  <Slider />
</template>

<style>
:root {
  --dark-blue: hsl(227, 35%, 25%);
  --gray-blue: hsl(225, 20%, 60%);
  --bg-white: hsl(230, 100%, 99%);
}

#app {
  font-family: 'Manrope', sans-serif;
}

body {
  background: url('../src/images/bg-pattern.svg') no-repeat;
  background-size: 2400px 450px;
  background-color: var(--bg-white);
}
</style>
