<template>
  <div>
    {{ counter }}
 
    <div>
      <p></p>
      <button @click="pressAndDecrease()">-</button>
      <button @click="pressAndIncrease()">+</button> 
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const previousCount = localStorage.getItem('key') || 0
const counter = ref(previousCount)

const pressAndDecrease = () => {
  counter.value--
  localStorage.setItem('key', counter.value)
}

const pressAndIncrease = () => {
  counter.value++
  localStorage.setItem('key', counter.value)
}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
