<template>
  <form class="form">
    <my-input class="myinput" name="Nome: " number="3"/>
    <my-input class="myinput" name="Email: " />
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
  components: {
    MyInput,
    MyButton,
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
