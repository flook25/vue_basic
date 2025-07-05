<script setup>
import { ref } from 'vue'

const selectedOption = ref('')
const options = ref(['Option1', 'Option2', 'Option3'])
</script>

<template>
  <select v-model="selectedOption">
    <option v-for="option in options" :key="option">
      {{ option }}
    </option>
  </select>
</template>


