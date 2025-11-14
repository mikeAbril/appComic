<template>
   <div> 
    <div title = "" colorFondo = "" > </div>
   </div> 
</template>

<script setup>
import { defineProps } from 'vue';


const props = defineProps ({
    title:{
        type: String,
        description: String,      
    },
    coloFondo:{
        type: String,
        required: true,
        default: ""
    },
    
})
</script>