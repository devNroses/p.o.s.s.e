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
        <h1 class="pageTitle">Welcome Parents</h1>
        <p>
          Welcome to Parents of Students in Special Education, also known as
          P.O.S.S.E. We are here to assist you with your son or daughter’s
          educational needs and to empower you with the knowledge of how the
          educational maze is structured to ensure your child has a successful
          educational career.
        </p>
        <p>
          Our vision is to reduce the drop out rate for children with learning
          challenges that attend our public schools. P.O.S.S.E. is focused on
          progressively moving the child forward consistent with their
          educational grade level. The Mission of P.O.S.S.E. is to prevent the
          retention rate that creates a negative experience for a child that can
          impact them for a lifetime. [U.S.Department of Education Statistical
          Report].
        </p>
        <p>
          P.O.S.S.E.’s Mission is to create educational opportunities for
          children grades 1-12 with learning challenges by advocating for
          effective research-based learning programs that will promote the
          success and dignity of our children. When children with learning
          challenges can realize their right to education, this will have a
          lifelong and positive impact on their learning, achievement and
          employment opportunities.
        </p>
        <p>
          P.O.S.S.E.’s hero is Helen Keller. She overcame the struggle of being
          deaf and blind by never giving up, dedicated her life to help others,
          and made changes in the world despite her disabilities.... Keller is
          the power of perseverance to overcome great obstacles. One of the
          Themes in her Book is
          <b>“<u>The Power of the Right Kind of Education</u>”.</b>
        </p>
        <p>
          P.O.S.S.E. is premised on the belief that the key to effective
          educational programs for children with learning challenges is
          collaboration - as - equals by parents and educators. We look forward
          to working with you.
          <br /><br /><br /><i>Sincerely,</i>

          <br /><br /><br /><span
            >Marlena Vaughn, <br />CEO/Executive Program Director</span
          >
        </p>
        <p></p>
        <p></p>
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
              "url(" + require("@/assets/imgs/slide-img4.jpg") + ")",
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
    height: 650px;

    .slider {
      height: 100% !important;
      max-height: 650px !important;
      z-index: -1 !important;
    }
  }

  &-message {
    padding: 25px;
    display: flex;
    flex-direction: column;
    text-align: left;
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
      max-width: 800px;
      text-align: left;
    }

    img {
      margin-top: 10px;
    }
  }
}
</style>
