<script setup>
import { ref } from 'vue';

const price = ref(16);
</script>

<template>
  <main class="container">
    <div class="content">
      <span class="views">100K PAGEVIEWS</span>
      <span pricing-container>
        <span class="price">${{ price }}.00</span>
        <span class="month">/month</span>
      </span>
      <div class="slider-container">
        <input
          type="range"
          name="price-slider"
          class="slider"
          v-model="price"
          min="8"
          max="36"
        />
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
  box-shadow: 0 1px 15px rgba(0, 0, 0, 0.116);
  padding: 30px;
  border-radius: 5px;
  margin-top: 100px;
}

.slider-container {
  display: flex;
  justify-content: center;
  margin-top: 50px;
}

.views {
  margin-right: 80px;
  color: var(--gray-blue);
  letter-spacing: 1.9px;
  font-size: 12px;
}

.month {
  color: var(--gray-blue);
}

.price {
  font-size: 2.2rem;
  color: var(--dark-blue);
  font-weight: 800;
}
</style>
