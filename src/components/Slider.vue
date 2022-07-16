<script setup>
import { ref } from 'vue';

const price = ref(16.0);
</script>

<template>
  <main class="container">
    <div class="content">
      <span class="views">100K pageviews</span>
      <span class="price">${{ price }}.00/month</span>
      <div class="slider-container">
        <input type="range" name="price-slider" class="slider" v-bind="price" />
      </div>
    </div>
  </main>
</template>

<style>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 200px;
}

.content {
  background-color: white;
}
</style>
