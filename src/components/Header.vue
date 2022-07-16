<script setup>
import Slider from './Slider.vue';
</script>

<template>
  <header class="header-container">
    <div class="header-content">
      <h1 class="title">Simple trafic-based pricing</h1>
      <p class="sub-title">
        Sign-up for our 30-day trial. No credit card required.
      </p>
    </div>
  </header>
  <Slider />
</template>

<style>
.header-content {
  text-align: center;
  margin-top: 30px;
  color: var(--dark-blue);
  background-color: var(--bg-white);
  background: url('../images/pattern-circles.svg') no-repeat center;
  padding: 20px;
}

.sub-title {
  font-size: 15px;
  color: var(--gray-blue);
}
</style>
