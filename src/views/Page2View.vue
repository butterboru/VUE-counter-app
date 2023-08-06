<template>
  <div>
    {{ counter }}
  </div>
</template>

<script setup>
import { ref } from 'vue'

const previousCount = localStorage.getItem('key') || 0
const counter = ref(previousCount)

</script>
