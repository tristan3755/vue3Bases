<template>
    <article class="formulaire">
        <button v-on:click='changeToggle'>actvation</button>
        <div ref='element' class="formulaire">
        <p v-if="nom.length>3">{{nom}}</p>
        <input type="text" v-model="nom">
        <button v-on:click="submitt" type="submit">valide ma gueule </button>
        </div>
    </article>
</template>

<script>
import { ref,onMounted } from 'vue';

export default {
    setup(){
let nom=ref('')
let element=ref()
let nameValue
function submitt(){
     nameValue=`${nom.value}`
    console.log(nameValue)
    /*console.log('nom:'+nom.value)*/
}

return{
    nom,
    element,
    nameValue,
    submitt,
}
    },
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
