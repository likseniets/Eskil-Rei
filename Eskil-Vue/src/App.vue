<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>Klasser</h1>
    <Table></Table>
  </div>
</template>

<script>
import Table from "./components/Table";

export default {
  name: 'app',
  components: {
    Table
  }
}

</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
