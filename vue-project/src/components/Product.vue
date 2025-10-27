<script setup>
const props = defineProps({
    id : Number,
    name : String,
    price : Number,
    onAdd : Function,
})

const addToCard = () => {
    props.onAdd(props.id)
}
</script>

<template>
<div>
    <h2>{{ props.name }}</h2>
    <p>Preco : {{  props.price }}</p>
    <button @click="addToCard(props.id)">Buy</button>
</div>
</template>

<style scoped>
div{
    padding: 1rem;
    width: 10rem;
    height: 13rem;
    display: flex;
    flex-direction: column;
    background-color: rgb(62, 62, 252);
    justify-content: space-around;
}
</style>