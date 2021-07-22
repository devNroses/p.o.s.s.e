<template>
  <footer>
    <div class="footer-wrapper">
      <div class="footer-copyright">
        <p>
          The educational consultants and advocates affiliated with Parents of
          Students in Special Education are not licensed to practice law. Thus,
          the services offered should not be considered legal representation.
          Further, all information provided by Parents of Students in Special
          Education should, in no way, be construed as providing legal advice.
          Information provided by the educational consultants and advocates is
          intended to be recommendations based on their knowledge and experience
          as well as the facts associated with each individual situation. All
          rights reserved. Copyright ©2011.
        </p>
      </div>
      <div class="footer-contact">
        <p><b>Call </b> <a href="tel:6193350536">619.335.0536</a></p>
        <p>
          <b>Email </b>
          <a href="mailto: marlena@possesandiego.org"
            >marlena@possesandiego.org</a
          >
        </p>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
$footerBackground: #849c7a;
$footerColor: #e4f0d8;

.footer {
  &-wrapper {
    display: flex;
    justify-content: space-between;
    padding: 25px;
    background-color: $footerBackground;
    color: #e4f0d8;
    bottom: 0;

    div {
      width: 380px;
    }
  }

  &-copyright {
    p {
      font-size: 12px;
      text-align: left;
      line-height: 1;
      margin: 20px auto;
    }
  }

  &-contact {
    p {
      font-size: 16px;
    }

    a {
      color: $footerColor;
      margin-left: 12px;
    }
  }
}
</style>
