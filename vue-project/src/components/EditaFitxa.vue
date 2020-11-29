    <template>
  <div class="hello">
    <h1>Edita Fitxa</h1>
    Identificador : {{ id }}
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    nores: String,
  },
  data() {
    return {
      id: "",
    };
  },
  mounted() {
    // Get params of url  xtoni
    this.id = this.$route.params.id;
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
