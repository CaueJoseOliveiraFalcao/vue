<script setup>
import { ref , watch } from 'vue';
const nascimento = ref(1900);
const anoAtual = ref(2000);
const idade = ref(0);

watch(anoAtual , (anoAtual) => {
    idade.value = anoAtual - nascimento.value;
})
watch(nascimento , (nascimento) => {
    idade.value = anoAtual.value - nascimento;
})
</script>

<template>
    <div>
        <h1>assistidas</h1>
        <p>{{ idade }}</p>
        <label for="">ano nascimento</label>
        <input type="number" min="1900" v-model="nascimento">
        <label for="">ano atual</label>
        <input type="number" min="2000" v-model="anoAtual">
    </div>
</template>

<style scoped>
</style>