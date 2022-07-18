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
  /* Primary  */
  --soft-cyan: hsl(174, 77%, 80%);
  --strong-cyan: hsl(174, 86%, 45%);
  --gray-red: hsl(14, 92%, 95%);
  --light-red: hsl(15, 100%, 70%);
  --pale-blue: hsl(226, 100%, 87%);

  /* Neutral */
  --bg-white: hsl(230, 100%, 99%);
  --light-gray-blue: hsl(224, 65%, 95%);
  --lg-blue: hsl(223, 50%, 87%);
  --gray-blue: hsl(225, 20%, 60%);
  --dark-blue: hsl(227, 35%, 25%);
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
