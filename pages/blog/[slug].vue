<script setup lang="ts">
const posts = [
  {
    slug: 'post-1',
    title: 'Post 1',
    contents: 'contents of post 1',
  },
  {
    slug: 'post-2',
    title: 'Post 2',
    contents: 'contents of post 2',
  },
  {
    slug: 'post-3',
    title: 'Post 3',
    contents: 'contents of post 3',
  },
]

const route = useRoute()
const title = ref('')
const contents = ref('')

const found = posts.find(post => post.slug === route.params.slug)
if (found) {
  title.value = found.title
  contents.value = found.contents
}
</script>

<template>
  <h2>{{ title }}</h2>
  <div>{{ contents }}</div>
</template>

<style scoped>

</style>