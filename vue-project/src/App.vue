<template>
  <div id="app">
    <header>
      <p>Aixo es el header. Va dins de App.vue</p>
      <img alt="Logo Classicoman" src="./assets/logo-classicoman-optim.png" />
    </header>

    <!-- vue-router  xtoni -->

    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/gestionaFitxes">GestionaFitxes</router-link>
    </div>
    <router-view />

    <!-- vue-router  xtoni -->

    <footer>Aixo es el footer</footer>
  </div>
</template>

<style>
/* xtoni */

header,
footer {
  background-color: aquamarine;
  padding: 20px 5px;
  display: flex;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
  background-color: lightcyan;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
