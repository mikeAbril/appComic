<template>
<div class="principal">
  <footer>
     <div class="q-pa-lg flex flex-center">
    <QPagination
      v-model="current"
      color="black"
      :max="10"
      :max-pages="6"
      :boundary-numbers="false"
    />
  </div>
  </footer>
</div>
</template>

<script setup>
import { ref } from 'vue';
import { QPagination } from 'quasar';

const current = ref(5)
</script>


<style>
</style>