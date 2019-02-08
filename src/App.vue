<template>
  <div id="app">
    <img width="466" height="72" src="https://i.ibb.co/bKRG5R4/logo.png" />
    <HelloWorld />
  </div>
</template>

<script>
import HelloWorld from "./components/pages/index";

export default {
  name: "App",
  components: {
    HelloWorld
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
