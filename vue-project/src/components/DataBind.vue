<script setup>
    import { ref } from 'vue';
    const valor = ref("vue");
</script>

<template>
    <div id="component">
        <input type="text" v-model="valor">
    </div>
</template>

<style scoped>

</style>