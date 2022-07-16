<script setup>
import { ref } from 'vue';

const price = ref(16);

const views = ref(100);
</script>

<template>
  <main class="container">
    <div class="content">
      <span class="views">{{ views }}K PAGEVIEWS</span>
      <span class="pricing-container">
        <span class="price">${{ price }}.00</span>
        <span class="month">/month</span>
      </span>
      <div class="slider-container">
        <input
          v-model="price"
          type="range"
          name="price-slider"
          class="slider"
          min="8"
          max="36"
          step="4"
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
  min-width: 400px;
}

.slider-container {
  display: flex;
  justify-content: center;
  margin-top: 50px;
}

.slider {
  width: 300px;
}

.views {
  margin-right: 80px;
  color: var(--gray-blue);
  letter-spacing: 1.9px;
  font-size: 15px;
}

.month {
  color: var(--gray-blue);
}

.price {
  font-size: 36px;
  color: var(--dark-blue);
  font-weight: 800;
}
</style>
