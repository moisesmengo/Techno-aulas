<template>
  <div id="app">
    <Header></Header>
    <router-view></router-view>
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
</style>
