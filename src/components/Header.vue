<template>
  <header>
    <nav>
      <div class="logo"><router-link to="/">Techno</router-link></div>
      <ul>
        <li><router-link to="/cursos">Cursos</router-link></li>
        <li><router-link to="/contato">Contato</router-link></li>
      </ul>
    </nav>
  </header>
</template>
<script>
export default {
  name: "Header",
};
</script>
<style scoped>
header {
  background-color: #234;
}
header a {
  color: aliceblue;
}
a.router-link-active {
  color: #4b8;
}
.logo a {
  color: aliceblue;
  font-size: 1.5rem;
}
nav {
  max-width: 800px;
  margin: 0 auto;
  display: flex;
  align-content: space-between;
  padding: 20px;
}
.logo {
  flex: 1;
}
ul li {
  display: inline-block;
}
li a {
  padding: 0 10px;
  margin-left: 10px;
}
</style>