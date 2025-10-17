<script setup>
import { defineProps } from 'vue';

defineProps({
    nome : String , 
    vachorros : Number
})
</script>

<template>  
    <div>
        <h1>condicao</h1>
        <p>nome : {{ nome }}</p>
        <P v-if="vachorros === 0">nao tem vachottos</P>
        <p v-else-if="vachorros === 1">tem um varchorros</p>
        <p v-else-if="vachorros > 1">tem muitos varchhorros</p>

    </div>
</template>

<style scoped>
</style>