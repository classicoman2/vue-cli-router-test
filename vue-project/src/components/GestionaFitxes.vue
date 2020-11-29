<template>
  <div class="hello">
    <h1>{{ titol }}</h1>
    <p>És un component nou</p>
    <div v-for="comanda in comandes" v-bind:key="comanda.id">
      <div class="rotul_comanda">
        Fitxa: #{{ comanda.id }} - Titol: {{comanda.titol}} - Autor: {{comanda.autor}}
        <button class="elimina_comanda" v-on:click="eliminaComanda(comanda.id)">
          Delete
        </button>

<!--        <button class="edita_comanda" v-on:click="editaComanda(comanda)">   -->
        <a href="#/editaFitxa/1">
          Edita
        </a>
      </div>
      <div v-for="item in comanda.items" v-bind:key="item.id">
        <div class="fila" v-bind:class="{ producte_car: item.preu >= 100 }">
          <span class="itemtext">{{ item.text }} - </span>
          <span class="itempreu">Preu: {{ item.preu }}€ - </span>
          <span class="itemunitats">Unitats: {{ item.unitats }}</span>
        </div>
      </div>

    </div>
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

      comandes: [],
    };
  },

  mounted() {
    /* Obté les comandes */
    this.obteComandes();
  },
  methods: {
    obteComandes: function () {
      fetch("http://localhost:3000/fitxes")
        .then((response) => response.json())
        .then((data) => {
          this.comandes = data;
        });
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
