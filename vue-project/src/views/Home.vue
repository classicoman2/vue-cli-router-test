<template>
  <div class="home">
    <HelloWorld msg="Missatge benvinguda (xtoni)" />
    <a href="#/gestionaFitxes">Link directe: vés a pagina de gestio de fitxes</a>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    HelloWorld,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
