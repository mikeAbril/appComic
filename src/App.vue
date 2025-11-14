<template>
    <div class="principal">
        <div class="card">
            <cards title="Desayuno" :image="desayuno" colorFondo=""></cards>
        </div>
        <div class="card">
            <cards title="Almuerzo" :image="almuerzo" colorFondo=""></cards>
        </div>
        <div class="card">
            <cards title="Cena" :image="cena" colorFondo=""></cards>
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
import cards from './components/cards.vue';
import desayuno from './assets/desayuno.png'
import almuerzo from './assets/almuerzo.png'
import cena from './assets/cena.png'

const tab = ref('comidas')


</script>


<style>
.card {
    border: solid 2px red;
    border-radius: 10px;
    width: 400px;
}
</style>