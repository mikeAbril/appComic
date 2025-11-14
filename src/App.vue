<template>
  <div class="principal">
    <footer>
      <div class="q-pa-md">
        <div class="q-gutter-y-md" style="margin: 0 auto">
          <q-tabs v-model="tab" class="text-teal">
            <q-tab name="comidas" icon="no_food" label="comidas" />
            <q-tab name="entrenamientos" icon="fitness_center" label="entrenamientos"/>
          </q-tabs>
          <!-- contenido   -->
          <q-tab-panels v-model="tab" animated>
            <q-tab-panel name="comidas">
              <div class="card">
                <cards title="Desayuno" :image="desayuno" colorFondo=""></cards>
              </div>
              <div class="card">
                <cards title="Almuerzo" :image="almuerzo" colorFondo=""></cards>
              </div>
              <div class="card">
                <cards title="Cena" :image="cena" colorFondo=""></cards>
              </div>
            </q-tab-panel>

            <q-tab-panel name="entrenamientos">
              <div class="entrenos">
                  <div class="card2">
                    <cards title="Lunes: Trotar"  colorFondo=""></cards>
                    <q-btn color="primary" label="Empezar Entreno" />
                  </div>
                  <div class="card2">
                    <cards title="Martes: pecho"   colorFondo=""></cards>
                    <q-btn color="primary" label="Empezar Entreno" />
                  </div>
                  <div class="card2">
                    <cards title="Miercoles: pierna"   colorFondo=""></cards>
                    <q-btn color="primary" label="Empezar Entreno" />
                  </div>
                  <div class="card2">
                    <cards title="Jueves: Espalda"   colorFondo=""></cards>
                    <q-btn color="primary" label="Empezar Entreno" />
                  </div>
                  <div class="card2">
                    <cards title="Viernes: Natacion"   colorFondo=""></cards>
                    <q-btn color="primary" label="Empezar Entreno" />
                  </div>
                </div>
            </q-tab-panel>
          </q-tab-panels>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>
import { ref } from "vue";

import cards from "./components/cards.vue";
import desayuno from "./assets/desayuno.png";
import almuerzo from "./assets/almuerzo.png";
import cena from "./assets/cena.png";

const tab = ref("comidas");

 

</script>

<style>
.card {
  border: solid 2px red;
  border-radius: 10px;
  width: 400px;
}
.card2{
  border: solid 1px #009688;
  border-radius: 10px;
  width: 1000px;
  display: grid;
  grid-template-columns: 1fr;
  justify-items: center;
  box-shadow: 1px 3px 2px 1px rgb(0, 0, 0,0.5);
}
.entrenos{
  display: grid;
  place-self: center;
  gap: 10px;
}
.q-btn{
  margin-bottom: 5px;
  
}
</style>
