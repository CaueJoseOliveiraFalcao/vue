<script setup>
import { ref  } from 'vue';
import { watchEffect } from 'vue';
const nascimento = ref(1900);
const anoAtual = ref(2000);
const idade = ref(0);

watchEffect(() => {
    idade.value = anoAtual.value - nascimento.value
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