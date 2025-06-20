<template>
    <div class="box has-text-weight-bold">
        <div class="columns">
            <div class="column is-7">
                Descricao da tarefa
            </div>
            <div class="column">
                <Cronometro tempoEmSegundos="14"/>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Cronometro from './Cronometro.vue';

    export default defineComponent({
        name: 'MenuTarefa',
        components:{ Cronometro}
    })
</script>

<style scoped>

.box{
    background: #2f00ff;
}

</style>