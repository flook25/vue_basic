<script setup>
import MyButton from '../src/components/MyButton.vue'; // Assuming you saved your button component as MyButton.vue
import ParentAndChild from './components/ParentAndChild.vue';

const handleEvnetFormChild = (message) => {
  alert('message');
}
</script>

<template>
  
    <ParentAndChild @myEvent="handleEvnetFormChild">

      <template #myHeader>
        <h1>Custom Header</h1>
      </template>

    </ParentAndChild>
  
</template>