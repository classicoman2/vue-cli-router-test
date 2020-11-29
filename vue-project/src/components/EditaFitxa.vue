    <template>
  <div class="hello">
    <h1>Edita Fitxa</h1>
    Identificador : {{ id }}

    <form>
      <div class="form-group">
        <label for="titol">titol</label>
        <input
          type="text"
          class="form-control"
          id="titol"
        />
      </div>
      <div class="form-group">
        <label for="autor">autor</label>
        <input
          type="text"
          class="form-control"
          id="autor"
        />
      </div>
      <button type="submit" class="btn btn-primary">Submit</button>
    </form>
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

    //Get fitxa
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

form {
  width:600px;
  margin-left:50px;
}

.form-group {
  display:flex;
}

label {
  margin-right: 20px;
}
</style>
