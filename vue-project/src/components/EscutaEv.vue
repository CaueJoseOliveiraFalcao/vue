<script setup>
import Emitee from './Emitee.vue';
import { ref } from 'vue';
const total = ref(0);
const adiciona = (preco) => {
    total.value += preco
}
</script>
<template>
    <div>
        <h1>escuta ev</h1>
        <p>total : {{ total }}</p>
        <Emitee item="item1" :preco="87" @foiAdicionado="adiciona"/>
        <Emitee item="item2" :preco="88" @foiAdicionado="adiciona"/>
        <Emitee item="item3" :preco="89" @foiAdicionado="adiciona"/>        
        <div>
        </div>
    </div>
</template>