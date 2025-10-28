<script setup>
import { ref } from 'vue';
let nav = ref('-168px');
const changeNav = () => {
    nav.value = nav.value === '-168px' ? '1px' : '-168px';
}
</script>

<template>
        <div class="lateral-bar" :style="{ right: nav}">
            <button @click="changeNav">volta</button>
        </div>
        <div class="main">
           <h1>Shop Test</h1>
           
           <div class="normal-head">
            <router-link to="/home"><a href="#">perfil</a></router-link>
            <router-link to="/carrinho"><a href="#">carrinho</a></router-link>
           </div>
           <div class="hamburguer">
            <button @click="changeNav">=</button>
           </div>

        </div>
</template>

<style scoped>
    .lateral-bar{
        position: fixed;
        background-color: rgb(214, 47, 47);
        width: 10rem;
        height: 100%;
        transition: all 0.3s;
    }
    .main{
        display: flex;
        padding: 1rem;
        justify-content: space-between;
        background-color: rgb(214, 47, 47);
        align-items: center;
    }
    a{
        text-decoration: none;
        margin: 0 1rem;
        color: white;
        font-size: 20px;
    }
    h1 {
        font-size: 35px;
        color: white;
    }
    .hamburguer{
        display: none;
    }
    @media (max-width : 768px) {
        h1{
            font-size: 25px;
        }
        a{
            font-size: 15px;
        }
        .normal-head{
            display: none;
        }
        .hamburguer{
            display: block;
        }
    }
</style>