<template>
  <div>
    {{ counter }}
  </div>
</template>

<script setup>
import { useStore } from 'vuex'
import { computed } from 'vue'

const store = useStore()

const counter = computed(() => store.state.counter)

</script>
