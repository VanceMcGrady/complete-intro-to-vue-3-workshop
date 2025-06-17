<script setup>
import { ref } from 'vue'
const count = ref(0)
function incrementCount() {
  count.value++
}
</script>

<template>
  <div class="wrapper">
    <h1>BaseCounter</h1>
    <button @click="incrementCount">You Clicked Me {{ count }} times</button>
  </div>
</template>

<style scoped>
.wrapper {
  background-color: blue;
}
</style>
