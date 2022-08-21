<script setup>
import { useMouse } from '@vueuse/core'
const {x, y} = useMouse();
</script>

<template>
  <div>x: {{x}}, y: {{y}}</div>
</template>

<style scoped>
</style>
