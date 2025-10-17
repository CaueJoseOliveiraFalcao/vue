<script setup>
import First from './components/First.vue';
import Header from './components/Header.vue';
import ComDados from './components/ComDados.vue';
import PrimitiveData from './components/PrimitiveData.vue';
import DataBind from './components/DataBind.vue';
import Props from './components/Props.vue';
import EscutaEv from './components/EscutaEv.vue';
import PropsComputeds from './components/PropsComputeds.vue';
import PropsAssistidas from './components/PropsAssistidas.vue';
import ReCondicional from './components/ReCondicional.vue';
import Listas from './components/Listas.vue';
const kai = 'kai'
const norar = 20;
const varchottos = [
   {nome : 'kaikai' , idade : 4},
   {nome : 'she so heavy' , idade : 7}
];
</script>

<template>
   <div>
      <Header/>
      <EscutaEv/>
      <Listas nome="au au" :vachorros="varchottos"/>
   </div>


</template>

<style scoped>
 

</style>
