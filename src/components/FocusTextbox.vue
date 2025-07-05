<script setup>
    import {ref} from 'vue';

    const textbox = ref(null);

    const focusTextbox = () => {
        textbox.value.focus();
    }


</script>


<template>
    <input type="text" v-model="text" ref="textbox" />
    <button @click = "focusTextbox">
        Focus Textbox
    </button>
</template>