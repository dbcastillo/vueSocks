<template>
  <div class="nav-bar"></div>
  <div class="product-display">
    <div class="product-container">
      <div class="product-image">
        <img :src="image" />
      </div>
      <div class="product-info">
        <h1>{{ product }}</h1>
        <p v-if="inventory > 10">In Stock</p>
        <p v-else-if="inventory <= 10 && inventory > 0">Almost sold out!</p>
        <p v-else>Out of Stock</p>
        <p v-if="onSale && inventory > 0">On Sale!</p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import socksGreenImage from './assets/images/socks_green.jpeg';
import socksBlueImage from './assets/images/socks_blue.jpeg';

const product = ref('Socks')
const image = ref(socksGreenImage)
const inventory = ref(1)
const onSale = ref(true)
</script>