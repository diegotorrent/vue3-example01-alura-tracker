<template>
<Temporizador />
</template> 

<script lang="ts">
import { defineComponent } from 'vue'
import Temporizador from './Temporizador.vue'
export default defineComponent({
    name: 'Formulario-home',
    components: {
        Temporizador
    }
    // /emits: ['aoTemporizadorFinalizado'],
    
}) 
</script>