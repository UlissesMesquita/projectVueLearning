<template>
    <div class="box">
        <div class="columns">
            <div class="columns is-8" role="form" aria-label="Fromulário para criação de uma nova tarefa">
                <input type="text" class="input" placeholder="Qual tarefa você deseja iniciar?">
            </div>
            <div class="is-flex is-align-items-center is-justify-content-space-between">
                <div class="column">
                    <section>
                        <strong>{{tempoDecorrido}}</strong>
                    </section>
                    <button class="button" @click="inciar()">
                        <span class="icon">
                            <i class="fas fa-play"></i>
                        </span>
                        <span>play</span>
                    </button>
                    <button class="button" @click="finalizar()">
                        <span class="icon">
                            <i class="fas fa-stop"></i>
                        </span>
                        <span>stop</span>
                    </button>
                </div>
            </div>
        </div>
    </div>

</template>

<script lang="ts">
import { defineComponent } from 'vue';
    
export default defineComponent({
    name: 'FormularioDashboard',
    data(){
        return {
            tempoEmSegundos: 0,
            cronometro: 0
        }
    },
    computed:{
        tempoDecorrido (): string{
            return new Date(this.tempoEmSegundos * 1000).toISOString().substr(11,8);
        }
    },
    methods: {
        inciar(){
            //Começar a Contagem
            //Contagem em ms
            this.cronometro = setInterval(() => {
                this.tempoEmSegundos += 1
            }, 1000)
            
        },
        finalizar() {
            clearInterval(this.cronometro)
        }
    }
})


</script>

<style>

</style>