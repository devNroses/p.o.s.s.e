<template>
  <nav class="nav-container">
    <div class="nav-logo">
      <span>P.O.S.S.E</span>
      <span>Parents of Students in Special Education</span>
    </div>

    <div>
      <ol>
        <li><NuxtLink to="/about">About</NuxtLink></li>
        <li><NuxtLink to="/services">Services</NuxtLink></li>
        <li><NuxtLink to="/tutoring">Tutoring</NuxtLink></li>
        <li><NuxtLink to="/faq">FAQ</NuxtLink></li>
        <li><NuxtLink to="/contact">Contact Us</NuxtLink></li>
      </ol>

      <div class="nav-mobile" @click.prevent="toggleShowMenu">
        <div></div>
        <div></div>
        <div></div>
      </div>

      <div
        class="nav-mobile-menu"
        :class="{ 'nav-mobile-menu-show': show }"
        @click.prevent="toggleShowMenu"
      >
        <div class="nav-mobile-menu-list">
          <ol>
            <li><NuxtLink to="/about">About</NuxtLink></li>
            <li><NuxtLink to="/services">Services</NuxtLink></li>
            <li><NuxtLink to="/tutoring">Tutoring</NuxtLink></li>
            <li><NuxtLink to="/faq">FAQ</NuxtLink></li>
            <li><NuxtLink to="/contact">Contact Us</NuxtLink></li>
          </ol>
        </div>
      </div>
    </div>
  </nav>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  data() {
    return {
      show: false
    };
  },
  methods: {
    toggleShowMenu() {
      this.show = !this.show;
    }
  }
});
</script>
<style lang="scss">
.nav {
  &-container {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    padding: 10px;
    color: #566050;

    a {
      color: #566050;
      font-size: 20px;
      transition: color 0.5s ease-in-out;
      text-decoration: none;

      &:hover {
        color: #bcddac;
      }
    }

    ol {
      display: flex;
      list-style: none;
      margin: 10px 0px;

      @media only screen and (max-width: 820px) {
        display: none;
      }

      li {
        font-size: 18px;
        padding: 0 16px;
      }
    }
  }
  &-logo {
    display: flex;
    flex-direction: column;
    span {
      &:first-child {
        font-size: 36px;
        font-weight: bold;
      }
      &:last-child {
        font-size: 16px;
        color: #111;
      }
    }
  }

  &-mobile {
    display: none;
    border: 1px solid #849c7a;
    padding: 10px;
    border-radius: 30%;
    transition: 0.5s ease-in-out;

    &:hover {
      background: #849c7a;
      cursor: pointer;
    }
    div {
      border: 1px solid #d5b9b2;
      border-radius: 20%;
      background: #d5b9b2;
      width: 20px;
      height: 2px;
      margin-bottom: 4px;

      &:last-child {
        margin-bottom: 0px !important;
      }
    }
    @media only screen and (max-width: 820px) {
      display: block;
    }

    &-menu {
      position: fixed;
      background: #849c7a;
      top: -200%;
      left: 0;
      right: 0;
      bottom: 0;
      width: 100%;
      height: 100%;
      display: flex;
      align-items: center;
      justify-content: center;
      transition: top 0.8s ease-in-out;

      &-show {
        top: 0;
      }

      &-list {
        width: 500px;
        display: flex;
        text-align: center;

        ol {
          display: flex;
          flex-direction: column;
          text-align: center;
          margin: 0 auto;

          li {
            padding: 0 !important;
            line-height: 1.5;
            a {
              font-size: 30px;
              font-weight: bold;
              text-transform: uppercase;
            }
          }
        }
      }
    }
  }
}
</style>
