<script setup>
import { ref } from 'vue'
const role = ref ('admin')
const count = ref(0)

function increment() {
    count.value++
}
function decrement() {
  count.value--
}
setTimeout(() => {
  role.value = 'HR'
}, 5000)
</script>

<template>
 <button @click="increment">Increment Value!</button>
 <!--<p>{{ count }}</p> -->
 <button @click="decrement">Decrement Value!</button>
 <p>{{ count }}</p>
 <br>
 <br>
 <h1>{{ role }}</h1>
</template>