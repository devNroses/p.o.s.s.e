<template>
  <footer>
    <div class="footer-wrapper">
      <div class="footer-contact" id="contact_section">
        <div class="footer-contact-info">
          <h3>How Can We Help?</h3>
          <p>
            If you have questions or want to inquire about our Program, please
            contact us by email or phone to set up a Zoom Conference call.
          </p>
          <div class="footer-contact-phone">
            <a href="tel:6193350536">Give Us a Call</a>
          </div>
          <div class="footer-contact-email">
            <a href="mailto: marlena@possesandiego.org">Send Us an Email</a>
          </div>
        </div>

        <div class="footer-contact-copyright">
          <p>
            The educational consultants and advocates affiliated with Parents of
            Students in Special Education are not licensed to practice law.
            Thus, the services offered should not be considered legal
            representation. Further, all information provided by Parents of
            Students in Special Education should, in no way, be construed as
            providing legal advice. Information provided by the educational
            consultants and advocates is intended to be recommendations based on
            their knowledge and experience as well as the facts associated with
            each individual situation. All rights reserved. Copyright ©2011.
          </p>
        </div>
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
    background-color: $footerBackground;
    color: #e4f0d8;
    bottom: 0;
    flex-wrap: wrap;
    width: 100%;
  }

  &-contact {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    margin: 0 auto;
    width: 100%;

    &-info {
      padding: 0 50px;
      width: 50%;
      display: flex;
      flex-wrap: wrap;
      padding: 15px 50px;

      h3 {
        font-size: 36px;
        font-weight: bolder;
        margin: 10px 8px 8px;
        text-align: left;
      }
      p {
        margin: 0 auto;
        font-size: 16px;
        font-style: italic;
        margin-bottom: 15px;
        text-align: left;
      }
    }

    &-phone,
    &-email {
      border-radius: 8px;
      width: 100%;
      max-width: 280px;
      height: 100px;
      color: #849c7a !important;
      display: flex;
      align-items: center;

      a {
        background-color: #383f34;
        border: 1px solid #383f34;
        border-radius: 10px;
        color: $footerColor;
        text-decoration: none !important;
        padding: 15px;
      }
    }

    &-copyright {
      width: 50%;
      p {
        font-size: 14px;
        text-align: left;
        line-height: 1.5;
        margin: 10px auto;
        width: 80%;
      }

      @media only screen and (max-width: 550px) {
        width: 100%;
      }
    }
  }
}
</style>
