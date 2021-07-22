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
        <h1>Welcome Parents</h1>
        <p>
          We are here to assist you with your son or daughter’s educational
          needs and to empower you with the knowledge of how the educational
          maze is structured so your child can be successful in their journey
          onto college.
        </p>
        <p>
          Our Vision is to reduce the drop out and retention rate for children
          with learning disabilities that attend our public schools. With this
          goal in mind, our Mission is to create educational opportunities for
          children grades 3-12 with learning disabilities by advocating for
          effective research-based learning programs that will promote the
          success and dignity of our children. P.O.S.S.E. also is here to assist
          with the development of these children into proficient and independent
          learners as they transition from high school to college.
        </p>
        <p>
          P.O.S.S.E is premised on the belief that the key to effective
          educational programs for children with learning disabilities is
          collaboration—as equals—by parents and educators.
        </p>
        <p>
          We look forward to working with you.
        </p>

        <img src="~/assets/imgs/POSSE_sig1.png" alt="Marlena Vaughn Director" />
        <span>Marlena Vaughn</span>
        <span> Executive Director</span>
      </div>
    </div>
    <Footer />
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
      height: 100% !important;
      max-height: 600px !important;
    }
  }

  &-message {
    padding: 25px;
    display: flex;
    flex-direction: column;
    text-align: center;
    justify-content: center;
    align-items: center;
    color: #111;
    background-color: #f0ebe6;

    h1 {
      font-size: 28px;
      margin-bottom: -5px;
    }
    p {
      line-height: 1.25;
      padding: 0 5px;
      margin-bottom: 5px;
      font-size: 16px;
      max-width: 600px;
    }

    img {
      margin-top: 10px;
    }

    span {
      &:last-child {
        font-size: 12px;
      }
    }
  }
}
</style>
