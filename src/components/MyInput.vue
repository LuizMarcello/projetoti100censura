<template>
  <div>
    <label for="myInput">{{ name }}</label>
    <input id="myInput" type="text" />
    <span>{{ number }}</span>
  </div>
</template>

<script>
export default {
  /* Declaração das "props" */
  /* "props"(propriedades).São do "pai" para o "filho" */
  /* São declaradas no componente "filho" */
  /* Tipos de props permitidos no Vue3:
     String, Number, Boolean, Array,
     Object, Date, Function, Symbol */
  /* Quando não precisa passar detalhes, como "type",
     "required", etc, pode ser declarada como um array
     de propriedades: */
  /* props: ["name", "number"], */
  props: {
    name: {
      type: String,
      required: true,
      /* default: "Ola", */
    },
    number: {
      type: String,
      required: true,
    },
  },
};
</script>

<style>
input {
  border: none;
  border-bottom: solid 1px grey;
  margin-top: 5%;
}
input:focus {
  outline-style: dotted;
  outline-color: #cacaca;
}
</style>
