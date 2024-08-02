<script setup lang="ts">
const menu = [
  {
    title: 'Product-1',
    path: '/shop/product-1',
  },
  {
    title: 'Product-2',
    path: '/shop/product-2',
  },
  {
    title: 'Product-3',
    path: '/shop/product-3',
  },
]
</script>

<template>
  <ul v-if="menu">
    <li v-for="(item, index) in menu" :key="index">
      <NuxtLink :to="item.path">{{ item.title }}</NuxtLink>
    </li>
  </ul>
</template>
