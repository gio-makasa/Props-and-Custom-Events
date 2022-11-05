<template>
  <li>
    <h2>Name: {{ name }}</h2>
    <h3>Age: {{ age }}</h3>
  </li>
</template>

<script>
export default {
  props: {
    id: { type: Number, require: true },
    name: { type: String, require: true },
    age: { type: Number, require: true },
  },
};
</script>

<style>
* {
  box-sizing: border-box;
}
li {
  text-align: center;
  border: 1px solid black;
  background-color: rgba(128, 128, 128, 0.4);
  border-radius: 8px;
  list-style-type: none;
  margin: 0 10px 10px 0;
}
ul h2{
  border-bottom: 1px dashed white;
  width: 100%;
}
</style>