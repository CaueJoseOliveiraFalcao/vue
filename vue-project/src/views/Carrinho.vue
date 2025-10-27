<script setup>
import CarrinhoProducts from '@/components/CarrinhoProducts.vue';

const carrinho = JSON.parse(localStorage.getItem('carrinho'));

</script>
<template>
    <section class="cards">
        <CarrinhoProducts  
        v-for="product in carrinho" 
        :id="product.id" 
        :name="product.name" 
        :price="product.price"/>
    </section>
     
</template>
<style scoped>
 .cards{
   display: flex;
   flex-direction: row;
   flex-wrap: wrap;
   width: 100%;
   gap: 1rem;
 }
</style>