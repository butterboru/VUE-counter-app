<template>
  <div>
    <button @click="pressAndDecrease()">-</button>
    <button @click="pressAndIncrease()">+</button> 
  </div>
</template>

<script setup>
import { useStore } from 'vuex'
import { computed } from 'vue'

const store = useStore()

const counter = computed(() => store.state.counter)

const pressAndDecrease = () => {
  store.commit('decrement')
}

const pressAndIncrease = () => {
  store.commit('increment')
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
