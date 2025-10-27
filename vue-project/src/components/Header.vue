<script>
</script>

<template>
        <div class="main">
           <h1>Shop Test</h1>
           
           <div>
            <router-link to="/home"><a href="#">perfil</a></router-link>
            <router-link to="/carrinho"><a href="#">carrinho</a></router-link>
           </div>
        </div>
</template>

<style scoped>
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
    @media (max-width : 768px) {
        h1{
            font-size: 25px;
        }
        a{
            font-size: 15px;
        }
    }
</style>