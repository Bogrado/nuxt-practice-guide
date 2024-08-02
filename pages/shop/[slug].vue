<script setup lang="ts">
const route = useRoute()
const product = reactive({
  title: '',
  contents: '',
})

let { title, contents } = toRefs(product)

const products = [
  {
    slug: 'product-1',
    title: 'Product-1',
    contents: 'contents-1',
  },
  {
    slug: 'product-2',
    title: 'Product-2',
    contents: 'contents-2',
  },
  {
    slug: 'product-3',
    title: 'Product-3',
    contents: 'contents-3',
  },
]

const found = products.find(item => item.slug === route.params.slug)
if (found) {
  product.title = found.title
  product.contents = found.contents
}
</script>

<template>
  <h2>
    {{ title }}
  </h2>
  <div>{{ contents }}</div>
</template>
