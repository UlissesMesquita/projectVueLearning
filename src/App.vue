<template>
  <main class="columns is-gapless is-multiline">
    <div class="column is-one-quarter">
        <barraLateral />
    </div>
    <div class="column is-three-quarter">
        ??????
    </div>
  </main>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

import barraLateral from './/components/barraLateral.vue'


export default defineComponent({
  name: 'App',
  components: {
    barraLateral  
  }
});
</script>

<style>

</style>
