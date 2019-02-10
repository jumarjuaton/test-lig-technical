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
/* global styles */
@import "./assets/styles/app.scss";

#app {
  font-family: "游ゴシック体", "Yu-Gothic", "Yu-Gothic-Light", Yu-Gothic,
    Yu-Gothic-Light, "ヒラギノ角ゴシック Pro", "Hiragino Kaku Gothic Pro",
    "メイリオ", Meiryo, Osaka, "ＭＳ Ｐゴシック", "MS PGothic", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
