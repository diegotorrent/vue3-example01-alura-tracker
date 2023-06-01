<template>
  <main class="columns is-gapless is-multiline">
    <div class="column is-one-quarter">
      <BarraLateral />
    </div>
    <div class="column is-three-quarter">
      <!-- <Formulario @aoSalvarTarefa="salvarTarefa" />
      <div class="lista">
        <Tarefa v-for="(tarefa, index) in tarefas" :tarefa="tarefa" :key="index"/>
      </div> -->
      <router-view></router-view>
      
    </div>
  </main>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import BarraLateral from './components/BarraLateral.vue';

export default defineComponent({
  name: 'App',
  components: {
    BarraLateral
  },
  data(){
    return{
      //tarefas: [] as ITarefa[]
    }
  },
  methods:{
    // salvarTarefa (tarefa: ITarefa) {
    //   this.tarefas.push(tarefa)
    // }
  }
});
</script>

<style>
.lista {
  padding: 1.25rem;
}
</style>
