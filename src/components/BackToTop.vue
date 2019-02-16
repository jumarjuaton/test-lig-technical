<template>
  <back-to-top>
    <button
      type="button"
      class="button-back-to-top"
      visibleoffset="200"
    ></button>
  </back-to-top>
</template>

<script>
import BackToTop from "vue-backtotop";

export default {
  name: "BackToTop",
  components: {
    BackToTop
  }
};
</script>

<style>
button.button-back-to-top {
  position: absolute;
  background: transparent url("https://i.ibb.co/gPqhQfn/icn-arrow-font-1-X.png")
    no-repeat 100% 100%;
  text-decoration: none;
  width: 24px;
  height: 14px;
  cursor: pointer;
  border: none;
  bottom: 65px;
  right: 410px;
  outline: none;
}
</style>
