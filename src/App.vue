<template>
  <div id="app">
    <Header></Header>
    <router-view class="container"></router-view>
  </div>
</template>
<script>
import Header from "./components/Header";
export default {
  components: { Header },
};
</script>
<style>
body {
  margin: 0px;
  font-family: "Xanh Mono", monospace;
  color: #234;
}
ul {
  list-style: none;
  padding: 0px;
  margin: 0px;
}
a {
  font-weight: bold;
  text-decoration: none;
  color: rgb(36, 48, 59);
}
img {
  max-width: 100%;
}
.container {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

.v-enter {
  opacity: 0;
  transform: translate3d(-20px, 0, 0);
}
.v-enter-active {
  transition: all 0.3s;
}
.conteudo {
  display: grid;
  grid-template-columns: 1fr minmax(200px, 400px);
  grid-gap: 30px;
}

@media screen and (max-width: 500px) {
  .conteudo {
    display: block;
  }
}
</style>
