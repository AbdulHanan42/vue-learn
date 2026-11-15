<script setup>
import { ref } from 'vue'

const isActive = ref(true)
</script>

<template>
  <h1 :class="isActive ? 'green' : 'red'">
    Hello World
  </h1>

  <button @click="isActive = !isActive">
    Change Color
  </button>
</template>

<style>
.green {
  color: green;
}

.red {
  color: red;
}
</style>