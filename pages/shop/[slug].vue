<script setup lang="ts">
const route = useRoute()
const product = reactive({
  title: '',
  contents: '',
  layout: null,
})

let { title, contents, layout } = toRefs(product)

const products = [
  {
    slug: 'product-1',
    title: 'Product-1',
    contents: 'contents-1',
    layout: 'dark',
  },
  {
    slug: 'product-2',
    title: 'Product-2',
    contents: 'contents-2',
    layout: 'light',
  },
  {
    slug: 'product-3',
    title: 'Product-3',
    contents: 'contents-3',
  },
]

const found = products.find(item => item.slug === route.params.slug)
title.value = found?.title
contents.value = found?.contents
layout.value = found?.layout
</script>

<template>
  <nuxt-layout :name="layout">
    <h2>
      {{ title }}
    </h2>
    <div>{{ contents }}</div>
  </nuxt-layout>
</template>
