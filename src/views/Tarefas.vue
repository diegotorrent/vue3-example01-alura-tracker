<template>
    <Formulario @aoSalvarTarefa="salvarTarefa" />
    <div class="lista">
        <Tarefa v-for="(tarefa, index) in tarefas" :tarefa="tarefa" :key="index"/>
    </div>
</template>
  
<script lang="ts">
import { defineComponent } from 'vue';
import Formulario from '../components/Formulario.vue';
import Tarefa from '../components/Tarefa.vue';
import ITarefa from '../interfaces/ITarefa' 

export default defineComponent({
name: 'App',
components: {
    Formulario,
    Tarefa
},
data(){
    return{
    tarefas: [] as ITarefa[]
    }
},
methods:{
    salvarTarefa (tarefa: ITarefa) {
    this.tarefas.push(tarefa)
    }
}
});
</script>
