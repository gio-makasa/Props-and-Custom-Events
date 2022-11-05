<template>
  <ul>
    <active-user
      v-for="user in users"
      :key="user.id"
      :name="user.name"
      :age="user.age"
    ></active-user>
  </ul>
  <user-data @data="add"></user-data>
</template>

<script>
export default {
  data() {
    return {
      users: [{ id: new Date().toISOString, name: "gio", age: 20 }],
    };
  },
  methods: {
    add(name, age) {
      const user = { id: new Date().toISOString, name: name, age: +age };
      this.users.push(user);
    },
  },
};
</script>

<style scoped>
* {
  box-sizing: border-box;
}
ul {
  width: 50%;
  float: left;
  padding: 0;
  margin: 0;
}
</style>