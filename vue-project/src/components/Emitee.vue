<script setup>
import { defineProps , defineEmits } from 'vue';
    const Props = defineProps({
        item : String,
        preco : Number
    })
    const emit = defineEmits(["foiAdicionado"]);
    const adicionar = () => {
        emit('foiAdicionado' , Props.preco);
    }
</script>
<template>
    <div class="component">
        <h1>emite</h1>
        <p>{{ item }} ,  {{ preco }}</p>
        <button @click="adicionar()">Adicionar ao carrinho</button>
    </div>
</template>
<style scoped>
div {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    height: 10rem;

}
h1{
        padding: 1rem;
    border-radius: 10px;
    background-color: brown;
    color: white;
    cursor: pointer;
}
h1:hover{
    opacity: 0.5;
}
</style>