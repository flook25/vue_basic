<script setup>
    import {ref} from 'vue';

    const childMessage = ref('Hello from parent');

    const handleClick = () => {
        childMessage.value = 'Hello from Child';
    }
const emit = defineEmits(['myEvent']);

const handleClickFromParent =() => {
    emit('myEvent', 'Hello from child');
}

</script>


<template>
    <h2>Parent component</h2>
    <p>{{ childMessage }}</p>
    <button @click="handleClick">Click Me</button>
    <button @click="handleClickFromParent">
        Click me from parent
    </button>
    <slot name="myHeader">Defult Header</slot>
</template>