<template>
  <nav class="nav-container">
    <div class="nav-logo">
      <span>P.O.S.S.E</span>
      <span>Parents of Students in Special Education</span>
    </div>

    <div>
      <ol>
        <li><NuxtLink to="/about">About</NuxtLink></li>
        <li><NuxtLink to="/sevices">Services</NuxtLink></li>
        <li><NuxtLink to="/tutoring">Tutoring</NuxtLink></li>
        <li><NuxtLink to="/faq">FAQ</NuxtLink></li>
        <li><NuxtLink to="/contact">Contact Us</NuxtLink></li>
      </ol>

      <div class="nav-mobile">
        <div></div>
        <div></div>
        <div></div>
      </div>
    </div>
  </nav>
</template>

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
      transition: 0.5s ease-in-out;
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
  }
}
</style>
