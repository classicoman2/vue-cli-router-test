<template>
  <div class="hello">
    <h1>{{titol}}</h1>
    <p>És un component nou</p>
  </div>
</template>

<script>
export default {
  name: "GestionaFitxes",
  props: {
    msg: String,
  },
  data() {
    return {
      titol: "Pagina de Gestio de Fitxes",
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
