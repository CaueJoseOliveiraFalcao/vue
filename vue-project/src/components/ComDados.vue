<script setup>
    const nome = "juuj"
    const code = "#MAE MAE"
</script>

<template>
 <div>
    <h1>Componente com dados</h1>
    <p>Nome : {{nome}} - {{ code }}</p>
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