<script setup>
    import {ref} from 'vue';

    const count = ref(0);
</script>


<template>
    <button @click="count++">Up</button>
    <button @click="count--">Down</button>

    <div>
        Counter: {{ count }}
    </div>


</template>