<template>
  <div>
    <div v-if="loading">
      <Loading />
    </div>
    <transition>
      <div v-if="api" class="conteudo">
        <div>
          <h1> {{api.nome}} </h1>
          <p> {{api.descricao}} </p>
          <h2>Aulas</h2>
          <ul class="aulas">
            <li v-for="aula in api.aulas" :key="aula.id">
              {{aula.nome}}
            </li>
          </ul>
        </div>
      </div>
    </transition>
  </div>
</template>
<script>
  import fetchData from "../mixins/fetchData";
  export default {
    name: 'Curso',
    props: ['curso'],
    mixins: [fetchData],
    created() {
      this.fetchData(`/curso/${this.curso}`)
    },
  }
</script>
<style>
  .aulas li {
    display: block;
    box-shadow: 0 2px 4px rgba(0, 0, 0, .1);
    background: #fff;
    margin-bottom: 10px;
    padding: 20px;
    border-radius: 4px;
  }
</style>