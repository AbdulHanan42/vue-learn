
<script setup>
import { reactive } from 'vue'

const user = reactive({
  name: 'Abdul hanan',
  isActive: true
})

function changeStatus() {
  user.isActive = !user.isActive
}
</script>

<template>
  <h1 :class="user.isActive ? 'green' : 'red'">
    Hello {{ user.name }}
  </h1>

  <p>{{ user.isActive ? 'Active' : 'Inactive' }}</p>

  <button @click="changeStatus">
    Change Status
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
