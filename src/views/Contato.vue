<template>
  <div class="contato">
    <div v-if="loading"><Loading /></div>
    <transition>
      <div v-if="api">
        <h1>Contato</h1>
        <p>{{ api }}</p>
      </div>
    </transition>
  </div>
</template>
<script>
import fetchData from "../mixins/fetchData";
export default {
  name: "Contato",
  mixins: [fetchData],
  created() {
    this.fetchData("/contato");
  },
};
</script>