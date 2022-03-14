<script setup>
const numbers = [1, 2, "Hello", { id:12, name: "John"}, 5, 6, 7, 8, 9];
</script>
 
<template>
  <div>
    <ul>
      <li v-for="(number, index) in numbers" :key="index">
        {{ index + " " + number }}
      </li>
    </ul>
  </div>
</template>
 
<style scoped></style>