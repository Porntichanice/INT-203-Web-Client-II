<script setup>
const isSearch = true
</script>
<template>
  <div v-show="isSearch">
    <label for="search">Search</label>
    <input type="text" id="search" class="border" />
  </div>
</template>
<style></style>