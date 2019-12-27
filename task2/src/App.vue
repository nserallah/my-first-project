<template>
  <div id="app">
    <pop-up>
      <template v-slot:slot-button>Sign in modal</template>
      <template v-slot:slot-body>
        <h3>Hello this modal for --sign in--</h3>
        <label for="username">Username
          <input id="username" type="text">
        </label>
        <label for="password">Password
          <input id="password" type="password">
        </label>
      </template>
    </pop-up>

    <pop-up>
      <template v-slot:slot-button>Sign Up modal</template>
      <template v-slot:slot-body>
        <h3>Hello this modal for --sign Up--</h3>
        <label for="firstname">First Name
          <input id="firstname" type="text">
        </label>
        <label for="lastname">Last Name
          <input id="lastname" type="text">
        </label>
        <label for="email">Your Email
          <input id="email" type="email">
        </label>
        <label for="notes">Your Notes
          <textarea id="notes"></textarea>
        </label>
      </template>
    </pop-up>

    <pop-up>
      <template v-slot:slot-button>Giv information</template>
      <template v-slot:slot-body>
        <h3>Hello this modal for --give you information--</h3>
        <h5>We have some information:</h5>
        <p>It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout. The point of using Lorem Ipsum</p>
      </template>
    </pop-up>
  </div>
</template>

<script>
export default {
 data: function () {
    return {
      
    }
  }
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

body {
  padding:0;
  margin:0;
}

* {
  box-sizing: border-box;
  margin:0;
  padding:0;
}
</style>
