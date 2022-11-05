<template>
  <form @submit.prevent="submited">
    <div>
      <label for="name">Name:</label>
      <input type="text" id="name" v-model="name" />
    </div>
    <div>
      <label for="age">Age:</label>
      <input type="text" id="age" v-model="age" />
    </div>
    <button>Add</button>
  </form>
</template>

<script>
export default {
  emits: ["data"],
  data() {
    return {
      name: "",
      age: "",
    };
  },
  methods: {
    submited() {
      this.$emit("data", this.name, this.age);
      this.name = "";
      this.age = "";
    },
  },
};
</script>

<style>
* {
  box-sizing: border-box;
}
form {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 50%;
  float: right;
  text-align: center;
  border: 1px solid black;
  background-color: rgba(128, 128, 128, 0.4);
  border-radius: 8px;
  padding: 20px;
}
form div {
  display: flex;
  flex-direction: column;
  width: fit-content;
  margin-bottom: 10px;
}
</style>