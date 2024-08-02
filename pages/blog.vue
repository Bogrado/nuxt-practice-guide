<script setup lang="ts">
const menu = [
  {
    title: 'Post 1',
    path: '/blog/post-1',
  },
  {
    title: 'Post 2',
    path: '/blog/post-2',
  },
  {
    title: 'Post 3',
    path: '/blog/post-3',
  },
]

const route = useRoute()
</script>

<template>
  <ul>
    <li v-for="item in menu" :key="item.title">
      <NuxtLink :to="item.path">{{ item.title }}</NuxtLink>
    </li>
  </ul>
  <NuxtPage :page-key="route.path" />
</template>
