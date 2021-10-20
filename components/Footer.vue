<template>
  <footer>
    <div class="footer-wrapper">
      <div class="footer-contact" id="contact_section">
        <div class="footer-contact-info">
          <h3>How Can We Help?</h3>
          <p>
            If you have any questions or would just like to inquire more about
            our program. Please contact us by phone or email to set up a zoom
            conference call.
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
    justify-content: space-between;
    background-color: $footerBackground;
    color: #e4f0d8;
    bottom: 0;
    flex-wrap: wrap;
    width: 100%;
  }

  &-contact {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin: 0 auto;
    width: 100%;

    &-info {
      padding: 0 50px;
      width: 50%;
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
      padding: 15px;

      h3 {
        font-size: 36px;
        font-weight: bolder;
        margin: 8px auto;
        text-align: center;
      }
      p {
        margin: 0 auto;
        font-size: 16px;
        font-style: italic;
        margin-bottom: 15px;
        text-align: center;
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
      justify-content: center;
      align-items: center;
      margin: 0 auto;

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
      p {
        font-size: 14px;
        text-align: left;
        line-height: 1.5;
        margin: 10px auto;
        width: 75%;
      }
    }
  }
}
</style>
