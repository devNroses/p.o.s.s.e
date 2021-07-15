<template>
  <nav class="nav-container">
    <div class="nav-logo">
      <span>P.O.S.S.E</span>
      <span>Parents of Students in Special Education</span>
    </div>

    <ol>
      <li>About</li>
      <li>Services</li>
      <li>Tutoring</li>
      <li>FAQ</li>
      <li>Contact Us</li>
    </ol>
  </nav>
</template>

<style lang="scss">
.nav {
  &-container {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    padding: 10px;

    ol {
      display: flex;
      list-style: none;

      li {
        padding: 0 8px;
      }
    }
  }
  &-logo {
    display: flex;
    flex-direction: column;
    span {
      &:first-child {
        font-size: 30px;
      }
      &:last-child {
        font-size: 16px;
      }
    }
  }
}
</style>
