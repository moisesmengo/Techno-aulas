<template>
  <div class="home">
    <div v-if="loading">
      CARREGANDO...
    </div>
    <div v-if="api">
      <h1>Home</h1>
      <p>{{api}}</p>
    </div>
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