<script setup lang="ts">
const menu = [
  { name: 'Home', path: '/home' },
  { name: 'About', path: '/about' },
]
</script>
<template>
  <nuxt-layout>
    <h1>Layouts and Pages</h1>
    <ul>
      <li v-for="item in menu" :key="item.path">
        <nuxt-link :to="item.path">{{ item.name }}</nuxt-link>
      </li>
    </ul>
    <nuxt-page />
  </nuxt-layout>
</template>
