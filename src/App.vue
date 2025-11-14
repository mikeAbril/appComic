<template>
<div class="principal">
    <div class="card">
        <cards title="Desayuno" :image="desayuno" colorFondo =""></cards>
    </div>
    <div class="card">
        <cards title="Almuerzo" :image="almuerzo" colorFondo =""></cards>
    </div>
    <div class="card">
        <cards title="Cena" :image="cena" colorFondo =""></cards>
    </div>

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
import cards from './components/cards.vue';
import desayuno from './assets/desayuno.png'
import almuerzo from './assets/almuerzo.png'
import cena from './assets/cena.png'

const current = ref(5)
</script>


<style>
.card{
    border: solid 2px red;
    border-radius: 10px;
    width: 400px;
}
</style>