<template>
  <div class="home">
    <div v-if="loading">
      <Loading />
    </div>
    <transition>
      <div v-if="api" class="conteudo">
        <div>
          <h1>Sobre a {{api.titulo}}</h1>
          <p>{{api.descricao}}</p>
          <router-link to="/cursos" tag="button" class="btn-cursos">Cursos</router-link>
          <div>
            <h2>Avaliações</h2>
            <ul>
              <li v-for="avaliacao in api.avaliacoes" :key="avaliacao.nome">
                <p>{{avaliacao.nome}}</p>
                <p>{{avaliacao.descricao}}</p>
              </li>
            </ul>
          </div>
        </div>
        <img src="../assets/05.png" alt="conhecimento">
      </div>
    </transition>
  </div>
</template>

<script>
  import fetchData from "../mixins/fetchData";
  export default {
    name: "Home",
    mixins: [fetchData],
    created() {
      this.fetchData("/home")
    },
  };
</script>
<style scoped>
  .btn-cursos {
    border: none;
    background-color: #4b8;
    border-radius: 4px;
    color: aliceblue;
    cursor: pointer;
    font-size: 1rem;
    margin-bottom: 40px;
    margin-top: 10px;
    font-family: "Xanh Mono", monospace;
    font-weight: bold;
    padding: 15px 20px;
    box-shadow: 0 4px 2px rgba(0, 0, 0, .1);
    transition: filter .5s all;
  }

  .btn-cursos:hover {
    filter: brightness(80%);
  }
</style>