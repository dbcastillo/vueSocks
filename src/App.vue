<template>
  <div class="nav-bar"></div>
  <div class="product-display">
    <div class="product-container">
      <div class="product-image">
        <img v-bind:src="socksGreenImage" />
      </div>
      <div class="product-info">
        <h1>{{ product }}</h1>
        <p>{{ description }}</p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import socksGreenImage from './assets/images/socks_green.jpeg';

const product = ref('Socks')
const description = ref('These socks are made from 100% cotton.')
</script>