<template>
    <article class="formulaire">
        <button v-on:click='changeToggle' v-if="toogle==false">activation</button>
        <button v-on:click='changeToggle' v-if="toogle==true">desactivation</button>
        <div  class="formulaire" v-if="toogle==true">
        <p v-if="nom.length>3">{{nom}}</p>
        <input type="text" v-model="nom">
        <button v-on:click="submitt" type="submit">valide ma gueule </button>
        </div>
    </article>
</template>

<script setup>
import { ref,onMounted } from 'vue';

let nom=ref('')
let nameValue
let toogle=ref(false)
function submitt(){
nameValue=`${nom.value}`
console.log(nameValue)
}
function changeToggle(){
toogle.value=!toogle.value
console.log(toogle)
}
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

</style>
