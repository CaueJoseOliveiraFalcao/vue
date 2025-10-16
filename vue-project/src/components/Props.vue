<script setup>
import { defineProps } from 'vue';
    defineProps({
        item : String,
        preco : Number
    })
</script>
<template>
    <div class="component">
        <h1>props</h1>
        <p>{{ item }} ,  {{ preco }}</p>
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