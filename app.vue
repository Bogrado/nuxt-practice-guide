<template>
  <h1>Layouts and pages</h1>
  <ul v-if="menu">
    <li v-for="(item, index) in menu" :key="index">
      <NuxtLink :to="item.path">{{ item.title }}</NuxtLink>
    </li>
  </ul>
  <NuxtPage />
</template>

<script setup>
const menu = [
  {
    title: 'Home',
    path: '/',
  },
  {
    title: 'About',
    path: '/about',
  },
  {
    title: 'Shop',
    path: '/shop',
  },
  {
    title: 'Blog',
    path: '/blog',
  },
]
</script>
