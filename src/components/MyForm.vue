<template>
  <form class="form">
    <my-input class="myinput" name="Nome: " @click="changeColor" />
    <my-input class="myinput" name="Email: " number="3" />
    <my-input class="myinput" name="Fone: " />
    <my-input class="myinput" name="Senha: " />
    <my-button class="mybutton" />
  </form>
</template>

<script>
import MyInput from "./MyInput.vue";
import MyButton from "./MyButton.vue";

export default {
  /* Componentes importados */
  /* Objeto de componentes */
  components: {
    MyInput,
    MyButton,
  },
  /* Objeto dos métodos */
  methods: {
    changeColor() {
      /* $emit: Para o evento ser ouvido.
         "$emit"(eventos).São do filho para o pai
         Dispara eventos para serem ouvidos e 
         disparados em outros componentes (*No pai)
         Existem eventos normais, como "click", onChange, etc.
         Este "Coloring", gerado pelo $emit, é um "evento
         personalizado" */
      this.$emit("Coloring");
    },
  },
};
</script>

<style>
.form {
  border: solid 1px grey;
  border-radius: 10px;
  width: 50%;
}
.mybutton {
  margin-top: 4%;
  margin-bottom: 4%;
  margin-left: 4%;
}
.myinput {
  margin-left: 4%;
}
</style>
