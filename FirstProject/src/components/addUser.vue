<template>
  <div>
    <h2>Hello, welcome to my first project</h2>
    <ul>
      <li v-for="(user, index) in users" :key="index">
        {{ user }}
        <button @click="deleteUser(user)">Delete Name</button>
      </li>
      <li v-if="newUser">{{ newUser }}</li>
    </ul>
    <div
      v-bind:class="{color: color}"
      v-for="(error, index) in messageErrors"
      :key="index"
    >{{ error }}</div>
    <input @keyup.enter="addUser()" type="text" v-model="newUser" />
    <button @click="addUser()">Add User</button>
  </div>
</template>

<script>
export default {
  name: "addUser",
  data: function() {
    return {
      users: ["Nserallah", "Ahmed", "Shadi"],
      newUser: "",
      color: true,
      messageErrors: [],
      maxChar: 15
    };
  },
  methods: {
    deleteUser: function(user) {
      var userIndex = this.users.indexOf(user);
      this.users.splice(userIndex, 1);
    },
    addUser: function() {
      this.messageError = [];

      if (!this.newUser) {
        this.messageErrors.push("this field cant be emty");
      } else if (!isNaN(this.newUser)) {
        this.messageErrors.push("this field cant be number");
      } else if (this.newUser.length > this.maxChar) {
          this.messageErrors.push("the field character cant more than 15")
      }

      this.users.push(this.newUser);
      this.newUser = "";
    }
  }
};
</script>

<style scoped>
.color {
  color: #f00;
}
</style>
