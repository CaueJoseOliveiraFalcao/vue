<script setup>
import { ref , computed } from 'vue';
const nascimento = ref(1900);
const anoAtual = ref(2000);
const idade = computed(() => {
    return anoAtual.value - nascimento.value
})
</script>

<template>
    <div>
        <h1>computado</h1>
        <p>{{ idade }}</p>
        <label for="">ano nascimento</label>
        <input type="number" min="1900" v-model="nascimento">
        <label for="">ano atual</label>
        <input type="number" min="2000" v-model="anoAtual">
    </div>
</template>

<style scoped>
</style>