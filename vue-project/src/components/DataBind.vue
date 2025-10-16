<script setup>
    import { ref } from 'vue';
    const valor = ref("vue");
</script>

<template>
    <div id="component">
        <p>{{ valor }}</p>
        <input type="text" v-model="valor" @input="(e)=>valor = e.target.value">
    </div>
</template>

<style scoped>
div{
    display: flex;
    justify-content: center;
    height: 10rem;
}
</style>