<script setup>
import Product from '@/components/Product.vue';


const products = [
   {id  : 1 , name : 'aboba' , price : 12},
   {id  : 2 , name : 'cere' , price : 112},
   {id  : 3 , name : 'abobwa' , price : 1532},
   {id  : 4 , name : 'abadsfoba' , price : 11112},
   
]

const carrinho = JSON.parse(localStorage.getItem('carrinho')) || [];

const salvarCarrinho = () =>{
   localStorage.setItem('carrinho' , JSON.stringify(carrinho))
}

const foiAdicionado = (id) =>{
   const product = products.find(p => p.id === id);
   carrinho.push(product);
   salvarCarrinho();
}
</script>

<template>
  <main>
          <section class="cards">
         <Product :onAdd="foiAdicionado" v-for="product in products" :id="product.id" :name="product.name" :price="product.price"/>
      </section>
      <router-link to="/carrinho">Carrinho</router-link>
  </main>
</template>

<style>
 .cards{
   display: flex;
   flex-direction: row;
   flex-wrap: wrap;
   width: 100%;
   gap: 1rem;
 }</style>