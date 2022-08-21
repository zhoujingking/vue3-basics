<script setup>
import {reactive, ref, computed, onMounted, onBeforeMount, onActivated} from 'vue'
const state = reactive({
  list: ['a', 'b', 'c']
})

const listCount = computed(() => {
  return state.list.length;
})

function onClick() {
  state.list.push('d')
}

onBeforeMount(() => {
  console.log('before mount')
})

onMounted(() => {
   console.log('mounted')
})

onActivated(() => {
  console.log('activated')
})
</script>

<template>
  <button @click="onClick">test</button>
  <div>{{listCount}}</div>
</template>

<style scoped>
</style>
