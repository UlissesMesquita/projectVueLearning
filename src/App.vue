<template>
  <main class="columns is-gapless is-multiline">
    <div class="column is-one-quarter">
        <BarraLateral/>
    </div>
    <div class="column is-three-quarter">
        <FormularioDashboard/>
        <!-- Lista de Tarefas -->
    </div>
  </main>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import  BarraLateral  from './components/BarraLateral.vue';
import  FormularioDashboard  from './components/Formulario.vue';


import barraLateral from './/components/barraLateral.vue'


export default defineComponent({
  name: 'App',
  components: {
    BarraLateral,
    FormularioDashboard
  }
});
</script>

<style>

</style>
