<script setup>
import { defineProps } from 'vue';

defineProps({
    nome : String , 
    vachorros : Array
})
</script>

<template>  
    <div>
        <h1>lista</h1>
        <p>nomeu : {{ nome }}</p>
        <ul>
            <li v-for="vachorro in vachorros">Nome : {{ vachorro.nome }} | {{ vachorro.idade }}</li>
        </ul>
    </div>
</template>

<style scoped>
</style>