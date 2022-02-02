<script setup>
import { ref } from 'vue'
console.clear()
const msg = 'Hello'
// counter is a reactive variable
const counter = ref(1)
// setTimeout(() => console.log(++counter), 3000)
setInterval(() => console.log(++counter.value), 1000)
</script>
 
<template>
    <p>Counter: {{ counter}}</p>
</template>
 
<style>

</style>