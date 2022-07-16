<script setup>
import { ref } from 'vue';
</script>

<template>
  <header>
    <h1 class="title">Simple trafic-based pricing</h1>
    <p class="sub-title">
      Sign-up for our 30-day trial. No credit card required.
    </p>
  </header>
</template>

<style>
header {
  text-align: center;
  margin-top: 30px;
  color: var(--dark-blue);
  background-color: var(--bg-white);
  background: url('../images/pattern-circles.svg') no-repeat center;
  padding: 20px;
}

.sub-title {
  font-size: 0.9375rem;
  color: var(--gray-blue);
}
</style>
