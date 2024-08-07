<script setup>
import {ref} from "vue"

const age =ref(22)
defineProps(
    {
    name:{
    type:String,
    required:true,
}
    
})

</script>


<template>

<div class="contenu">
    <h1>Donne moi l'anne e naissance de {{ name }} si tu sais que sont age = {{ age }} ?</h1>
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