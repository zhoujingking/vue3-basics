<script setup>
import { ref } from 'vue'
import { useFocus } from '@vueuse/core'

const button = ref();
const input = ref();
const para = ref()
const { focused : buttonFocus } = useFocus(button);
const { focused : inputFocus } = useFocus(input);
const { focused : paraFocus } = useFocus(para);
</script>

<template>
  <button ref="button">target ref -- {{buttonFocus}}</button>
  <input type="text" ref="input" :value="inputFocus">
  <!-- tabindex is the key attribute to make div focusable -->
  <div ref="para" tabindex="0" >godking -- {{paraFocus}}</div>
</template>

<style scoped>
</style>
