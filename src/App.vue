<template>
  <div id="app">
    <img width="466" height="72" src="https://i.ibb.co/bKRG5R4/logo.png" />
    <Slider
      animation="fade"
      v-model="sliderValue"
      :duration="5000"
      :speed="1000"
    >
      <SliderItem
        v-for="(i, index) in list"
        :key="index"
        @click="changeIndex(1);"
        :style="i"
      >
        <p style="line-height: 280px; font-size: 5rem; text-align: center;">
          Page{{ index + 1 }}
        </p>
      </SliderItem>
    </Slider>
  </div>
</template>

<script>
import Index from "./components/pages/Index";
import { Slider, SliderItem } from "vue-easy-slider";

export default {
  name: "App",
  components: {
    Index,
    Slider,
    SliderItem
  },
  data() {
    return {
      list: [],
      sliderValue: 2
    };
  },
  methods: {
    changeIndex(index) {
      this.sliderValue = index;
    }
  },
  mounted() {
    setTimeout(
      () =>
        (this.list = [
          {
            backgroundColor: "#3f51b5",
            width: "100%",
            height: "100%"
          },
          {
            backgroundColor: "#eee",
            width: "100%",
            height: "100%"
          },
          {
            backgroundColor: "#f44336",
            width: "100%",
            height: "100%"
          },
          {
            backgroundColor: "#eee",
            width: "100%",
            height: "100%"
          }
        ]),
      1000
    );
  }
};
</script>

<style lang="scss">
@import "./assets/styles/app.scss";
@import "./assets/styles/vendor.scss";

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
