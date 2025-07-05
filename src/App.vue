<script setup>
import MyButton from '../src/components/MyButton.vue'; // Assuming you saved your button component as MyButton.vue
import DropdownListAndArray from './components/DropdownListAndArray.vue';
import CheckAndRadio from './components/CheckAndRadio.vue';
import FocusTextbox from './components/FocusTextbox.vue';

const handleEvnetFormChild = (message) => {
  alert('message');
}
</script>

<template>
  
    <FocusTextbox />

</template>