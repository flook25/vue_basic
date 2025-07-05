<script setup>
    import {ref} from 'vue';

    const isDisaled = ref(false);
</script>

<template>
    <input type="checkbox" v-model="isDisaled"> Disable Button
    <button :disabled="isDisaled">Submit</button>
    <p>Is disabled: {{ isDisaled }}</p>

</template>