<script setup>
import { ref, watch } from 'vue';

const price = ref(16);

const views = ref('100K');

const addDiscount = ref(false);

const handleClick = () => {
  addDiscount.value = !addDiscount.value;
  console.log(addDiscount.value);
};

watch(price, (newPrice) => {
  if (newPrice == 8) views.value = '10K';
  if (newPrice == 12) views.value = '50K';
  if (newPrice == 16) views.value = '100K';
  if (newPrice == 20) views.value = '200k';
  if (newPrice == 24) views.value = '500K';
  if (newPrice == 28) views.value = '600K';
  if (newPrice == 32) views.value = '700K';
  if (newPrice == 36) views.value = '1M';
});
</script>

<template>
  <main class="container">
    <div class="content">
      <div class="pricing">
        <span class="views">{{ views }} PAGEVIEWS</span>
        <span class="price">${{ price }}.00</span>
        <span class="month">/month</span>
      </div>

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
      <div class="toggle-container">
        <span class="billing">Monthly billing</span>
        <div class="toggle-btn">
          <label class="switch">
            <input type="checkbox" @click="handleClick" />
            <span class="toggle round"></span>
          </label>
        </div>
        <span class="billing">Yearly billing</span>
        <span class="discount">25% discount</span>
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
  margin-top: 90px;
}

.content {
  background-color: white;
  box-shadow: 0 1px 15px rgba(0, 0, 0, 0.116);
  padding: 40px;
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
  width: 500px;
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

.pricing {
  text-align: center;
}

.toggle-container {
  margin-top: 80px;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 20px;
}

.switch {
  position: relative;
  display: inline-block;
  width: 60px;
  height: 34px;
}

.switch input {
  opacity: 0;
  width: 0;
  height: 0;
}

.toggle {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #ccc;
  -webkit-transition: 0.4s;
  transition: 0.4s;
  width: 60px;
}

.toggle:before {
  position: absolute;
  content: '';
  height: 26px;
  width: 26px;
  left: 4px;
  bottom: 4px;
  background-color: white;
  -webkit-transition: 0.4s;
  transition: 0.4s;
}

input:checked + .toggle {
  background-color: #2196f3;
}

input:focus + .toggle {
  box-shadow: 0 0 1px #2196f3;
}

input:checked + .toggle:before {
  -webkit-transform: translateX(26px);
  -ms-transform: translateX(26px);
  transform: translateX(26px);
}

.toggle.round {
  border-radius: 34px;
}

.toggle.round:before {
  border-radius: 50%;
}
</style>
