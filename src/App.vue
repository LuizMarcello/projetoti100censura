<template>
  <div class="main">
    <h1>{{ title }}</h1>
    <!-- "Coloring": Capturando este evento personalizado
         emitido pelo "$emit" no componente MyForm -->
    <!-- Com v-bind (":") é dinâmica -->
    <my-form @Coloring="myColor" :class="customColor" />
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
      customColor: "",
    };
  },

  methods: {
    myColor() {
      this.customColor = "coloring";
    },
  },
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
.coloring {
  background: rgb(2, 0, 36);
  background: linear-gradient(90deg, rgba(2, 0, 36));
  color: white;
}
</style>
