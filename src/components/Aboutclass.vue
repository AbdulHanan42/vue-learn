<script setup>
import { ref } from 'vue'
const className = ref('value pass from two way binding ')
const className2 = ref('value pass one way binding ')

</script>
<template>
<input type="text" v-model="className" placeholder="Enter class name" />
<p>{{ className }}</p>

<h1>One Way binding</h1>
<input type="text" v-bind:value="className2" placeholder="Enter another class name" />
<p>{{ className2 }}</p>
</template>
<style></style>