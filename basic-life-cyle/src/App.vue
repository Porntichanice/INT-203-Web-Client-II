
<script setup>
import { ref, onBeforeMount, onMounted } from 'vue'
onMounted(() => {
  alert('on mounted: ${num.value}')
  num.value = 10
  
})
onBeforeMount(() => {
  alert('on before mount: ${num.value}')
  num.value =5
})
onBeforeUpdate(() => {
  num.value = num.value > 5 ? 1 : num.value
  alert('on before update: ${num.value}')
})
onupdated(() => alert('on updated: ${num.value}'))
const num = ref(1)
alert('on created: ${num.value}')
</script>
 
<template>
  <div>
    num: {{ num }}
    <button @click="num = num + 1">+</button>
    <div>
      <NumUpdate :currentNum="num"/>
      <button @click="unShow">Not Show Current Num</button>
    </div>
  </div>

</template>
 
<style></style>