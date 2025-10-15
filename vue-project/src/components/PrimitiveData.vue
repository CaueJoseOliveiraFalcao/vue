<script setup>
    import { reactive } from 'vue';
    const obj = reactive({
        nome : 'ana',
        idade : 24
    });

    const name = () => {
        obj.nome ='kkkk';
    }
    const aniversario = () => {
        obj.idade +=1;
    }
</script>

<template>
    <div>
        <h1>Dados Reativcos</h1>
        <p>nome : {{ obj.nome }} | idade : {{ obj.idade }}</p>
        <button @click="aniversario()">Fazer Aniversario</button>
        <button @click="name()">mudar nome</button>
    </div>
</template>

<style scoped>
    div{
        text-align: center;
        border: 2px solid green;
        background-color: blue;
        border-radius: 15px;
        margin: 30px;
        padding: 10px;
    }
</style>