<script setup lang="ts">
import BaseCounter from './views/BaseCounter.vue'
</script>

<template>
  <main>
    <router-view />
    <BaseCounter />
  </main>
</template>

<style scoped>
html {
  background-color: blue;
}
</style>
