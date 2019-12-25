<template>
  <div id="app">
    <add-user></add-user>
    <incr-com></incr-com>
    <date-now :age="age"></date-now>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      age: 26
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
