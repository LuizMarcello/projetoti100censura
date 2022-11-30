<template>
  <div>
    <label for="myInput">{{ name }}</label>
    <input id="myInput" type="text" />
  </div>
</template>

<script>
export default {
  /* As "props" */
  props: {
    name: {
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
