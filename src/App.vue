<template>
  <div id="app"><Index /></div>
</template>

<script>
import Index from "./components/Index";

export default {
  name: "App",
  components: {
    Index
  }
};
</script>

<style lang="scss">
/* app styles */
@import "./assets/styles/app.scss";

#app {
  font-family: "Yu-Gothic", "Yu-Gothic-Light", Yu-Gothic, Yu-Gothic-Light,
    sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
