<template>
  <div class="dark">
    <p>dark</p>
    <slot />
  </div>
</template>

<style scoped>
.dark {
  background-color: #666;
}
.dark a {
  color: white;
}
</style>
