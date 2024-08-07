<script setup>
import {ref,onMounted} from "vue"
import frist_component from '@/components/frist_compnent.vue'


const name =ref("Moz")
onMounted(async function  requete (){

    console.log(`the component is now mounted.`)

    const req=await fetch("http://62.72.5.95:1999/notes")
    const json=await req.json()
    console.log(json);
    console.log(json.notes[0])

    for(let i=0;i<json.notes.length;i++){
        console.log("pp");
        console.log(json.notes[i])
      
    }})



</script>


<template>

<div class="contenu">
   <frist_component :name="name"/>
</div>

</template>




<style>
.contenu{
background-color: blue;
}

h1{
    font-size: 18px;
}

</style>