<template>
<div ref='element' class="formulaire">
    <p v-if="nom.length>3">{{nom}}</p>
    <input type="text" v-model="nom">
    <button v-on:click="submitt" type="submit">valide ma gueule </button>
</div>
</template>


<script setup>
import { ref,onMounted } from 'vue';

let nom =ref('')
let element=ref()
function submitt(){
    console.log(`nom=${nom.value}`)
    /*console.log('nom:'+nom.value)*/
}
onMounted(()=>{
element.value.classList='active'
})
</script>


<style>
.formulaire{
    height: 20vh;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
}
.active{
    background-color: aquamarine;
}
</style>
