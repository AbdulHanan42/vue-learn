<script setup>
import { ref } from 'vue'
let role = ref('admin')
const count = ref(0)

function increment() {
  count.value++
}
function decrement() {
  count.value--
}
setTimeout(() => {
  role.value = 'HR'
}, 2000)
console.log('role', role.value)
</script>

<template>
  <button @click="increment">Click here!
    {{ count }}
  </button>
  <button @click="decrement">Click here!
    {{ count }}
  </button>
  <p>Current role: {{ role }}</p>
</template>