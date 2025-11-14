<template>
    <div class="principal">
        <h1>{{ }}</h1>
        <div class="parteUno">
            <div class="card">
                <cards title="Desayuno" :image="desayuno" colorFondo=""></cards>
                <botones @accion ="agregar" colorFondo = "red" textoColor = "black" nombreBoton="Agregar Alimento"></botones>
            </div>
            <div class="card">
                <cards title="Almuerzo" :image="almuerzo" colorFondo=""></cards>
                <botones @accion ="agregar" colorFondo = "red" textoColor = "black" nombreBoton="Agregar Alimento"></botones>
            </div>
            <div class="card">
                <cards title="Cena" :image="cena" colorFondo=""></cards>
                <botones @accion ="agregar" colorFondo = "red" textoColor = "black" nombreBoton="Agregar Alimento"></botones>
            </div>
            <div class="card">
                <cards title="Bebidas" :image="bebidas" colorFondo=""></cards>
                <botones @accion ="agregar" colorFondo = "red" textoColor = "black" nombreBoton="Agregar Alimento"></botones>
            </div>
        </div>
        <footer>
            <div class="q-pa-md">
                <div class="q-gutter-y-md" style="max-width: 600px">
                    <q-tabs v-model="tab" class="text-teal">
                        <q-tab name="Comidas" icon="alarm" label="Alarms" />
                        <q-tab name="Entrenamientos" icon="movie" label="Movies" />
                    </q-tabs>
                    <!-- contenido   -->
                    <q-tab-panels v-model="tab" animated>
                        <q-tab-panel name="mails">
                            <h4>Mails content</h4>
                        </q-tab-panel>

                        <q-tab-panel name="comidas">
                            <h4>Alarms content</h4>
                        </q-tab-panel>

                        <q-tab-panel name="entrenamientos">
                            <h4>Movies content</h4>
                        </q-tab-panel>
                    </q-tab-panels>
                </div>
            </div>
        </footer>
    </div>
</template>

<script setup>
import { ref } from 'vue';
import cards from './components/cards.vue';
import botones from './components/botones.vue';
import desayuno from './assets/desayuno.png';
import almuerzo from './assets/almuerzo.png';
import cena from './assets/cena.png';
import bebidas from './assets/bebidas.png';

const tab = ref('comidas')

function agregar(){
console.log("");

}
</script>


<style>
.parteUno {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 15px;
}

.card {
    display: grid;
    justify-content: center;
    align-content: center;
    border: solid 2px #009688;
    border-radius: 10px;
    width: 400px;
}

.card h2 {
    font-size: 35px;
    text-align: center;
}

.card img {
    width: 230px;
    border: solid 1px;
    border-radius: 50%;
}
</style>