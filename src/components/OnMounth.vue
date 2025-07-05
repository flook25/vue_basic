<script setup>
    import { ref , onMounted } from 'vue';

    const month = ref('January');

    onMounted(() => {
        month.value = 'Febuary'
    })

</script>


<template>
    <p>selected month: {{ month }}</p>

</template>