<template>
  <AppHeader />
</template>

<script>
import Index from "./pages/Index";
import AppHeader from "./components/AppHeader";

export default {
  name: "App",
  components: {
    Index,
    AppHeader
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
