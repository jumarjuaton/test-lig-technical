<template>
  <header>
    <div class="header__div-logo">
      <img width="466" height="72" src="https://i.ibb.co/bKRG5R4/logo.png" />
    </div>
    <Slider
      width="1400px"
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
        <img width="1400" height="420" src="../assets/images/img-slider.jpg" />
      </SliderItem>
    </Slider>
  </header>
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
      sliderValue: 0
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
