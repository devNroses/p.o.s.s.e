<template>
  <div>
    <Nav />

    <div class="landing-container">
      <div class="landing-slider">
        <Slider
          animation="fade"
          v-model="sliderValue"
          :duration="7000"
          :speed="1000"
        >
          <SliderItem
            v-for="(i, index) in list"
            :key="index"
            @click="changeIndex(1)"
            :style="i"
          >
          </SliderItem>
        </Slider>
      </div>
      <div class="landing-message">
        [message]
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import { Slider, SliderItem } from "vue-easy-slider";

export default Vue.extend({
  components: {
    Slider,
    SliderItem
  },
  data() {
    const list: any[] = [];
    return {
      list,
      sliderValue: 2
    };
  },
  methods: {
    changeIndex(index: number) {
      this.sliderValue = index;
    }
  },
  mounted() {
    setTimeout(
      () =>
        (this.list = [
          {
            backgroundImage:
              "url(" + require("@/assets/imgs/slide-img1.jpg") + ")",
            backgroundRepeat: "no-repeat",
            backgroundSize: "cover",
            backgroundPosition: "center",
            width: "100%",
            height: "100%"
          },
          {
            backgroundImage:
              "url(" + require("@/assets/imgs/slide-img2.jpg") + ")",
            backgroundRepeat: "no-repeat",
            backgroundSize: "cover",
            backgroundPosition: "center",
            width: "100%",
            height: "100%"
          },
          {
            backgroundImage:
              "url(" + require("@/assets/imgs/slide-img3.jpg") + ")",
            backgroundRepeat: "no-repeat",
            backgroundSize: "cover",
            backgroundPosition: "center",
            width: "100%",
            height: "100%"
          }
        ]),
      1000
    );
  }
});
</script>

<style lang="scss" scoped>
.landing {
  &-slider {
    height: 500px;

    .slider {
      height: 120% !important;
    }
  }
}
</style>
