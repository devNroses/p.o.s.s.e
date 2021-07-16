<template>
  <div>
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
