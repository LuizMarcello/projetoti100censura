<template>
  <div class="main">
    <h1>{{ title }}</h1>
    <my-form />
  </div>
</template>

<script>
import MyForm from "./components/MyForm.vue";

export default {
  name: "App",

  /* Componentes importados */
  components: {
    MyForm,
  },

  /* "Dados" e retorno dos dados */
  data() {
    return {
      title: "Course Vue3",
    };
  },

  methods: {},
};
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.main {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
