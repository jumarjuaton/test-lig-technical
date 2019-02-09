<template>
  <div id="app">
    <div class="container-logo">
      <img width="466" height="72" src="https://i.ibb.co/bKRG5R4/logo.png" />
    </div>
    <Slider
      width="1402px"
      height="420px"
      v-model="sliderValue"
      :autoplay="false"
      :touch="true"
      :duration="5000"
      :speed="1000"
    >
      <SliderItem
        v-for="(i, index) in list"
        :key="index"
        @click="changeIndex(1);"
        :style="i"
      >
        <img
          width="1402"
          height="420"
          src="https://i.ibb.co/GWd9ffR/img-slider.png"
        />
        <p style="line-height: 280px; font-size: 5rem; text-align: center;">
          Page{{ index + 1 }}
        </p>
      </SliderItem>
    </Slider>
  </div>
</template>

<script>
import { Slider, SliderItem } from "vue-easy-slider";

export default {
  name: "AppHeader",
  components: {
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
            width: "100%",
            height: "100%"
          },
          {
            width: "100%",
            height: "100%"
          },
          {
            width: "100%",
            height: "100%"
          }
        ]),
      1000
    );
  }
};
</script>

<style>
.container-logo {
  padding: 29px 0;
}
.slider {
  margin: 0 auto;
}
.slider .slider-indicator-icon {
  margin: 0 10px !important;
  background-color: #ffffff !important;
  width: 16px !important;
  height: 16px !important;
}
.slider .slider-indicator-active {
  background-color: #e7ba2f !important;
}
</style>
