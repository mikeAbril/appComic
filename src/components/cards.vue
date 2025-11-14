<template>
   <div> 
    <div title = "" color = "" > </div>
   </div> 
</template>

<script setup>
import { defineProps } from 'vue';


const props = defineProps ({
    title:{
        type: String,
        description: String,
        
    }
})
</script>