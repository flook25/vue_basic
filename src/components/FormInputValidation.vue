<script>

import {ref} from 'vue';

const name = ref('');
const nameError = ref('');

const handleSubmit = () => {
    if (name.value.length < 3) {
        nameError.value = 'Name must 3 characters';
    } else {
        nameError.value = '';
    }
}

</script>

<template>
    <form @submit.prevent="handleSubmit">
        <input type="text" v-model="name" />
        <p>{{ nameError }}</p>
        <button type="submit">Submit</button>
    </form>
</template>