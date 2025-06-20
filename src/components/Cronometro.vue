<template>
    <section>
        <strong class="display" :style="{ color: cor }">
            {{ tempoDecorrido }}
        </strong>
    </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'CronometroContador',
    props: {
        tempoEmSegundos: {
            type: Number,
            default: 0
        },
        cor: {
            type: String,
            default: 'var(--texto-primario)'
        }
    },
    computed: {
        tempoDecorrido (): string {
            return new Date(this.tempoEmSegundos * 1000).toISOString().substr(11,8)
        }
    },
})
</script>