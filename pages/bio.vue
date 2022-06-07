<template>
  <div>
    <Nav />
    <div class="bio-container">
      <div class="bio-content">
        <div>
          <h2 class="pageTitle">Bio</h2>
          <p>
            As a native of San Diego, I fell in love with doing charitable work
            for children through various commitments with different
            organizations. I believe that reading transforms a child's world.
            Also, I believe that reading for children is a critical step in how
            children can comprehend their world. I have a deep appreciation for
            how non-profits can improve the quality of education for children
            and I continued with my passion for charitable work to make a
            difference in a child's educational career. My passion was deeply
            developed when my son was diagnosed with Dyslexia and other Learning
            Challenges.
          </p>
          <p>
            My career as a paralegal spans 40 years working continuously in the
            legal field. I began educating myself to advocate for my son when
            faced with insurmountable obstacles in the educational system. My
            focus became Special Education Law to become an advocate working
            with parents and their children for 15 years assisting parents to be
            able to find their voice and have a seat at IEP Meetings. I continue
            to empower parents with knowledge and understanding in their child's
            educational journey through the IEP Process.
          </p>
          <p>
            My education includes graduating with a Certificate from the William
            & Mary Law School Advocacy Program and remain a lifetime Member of
            ISEA Alumni Group. I continued my education and graduated with a
            Certificate from University of San Diego Law School Special
            Education Advocacy Program and remain a lifetime Member of the
            Alumni Group. I am a member and have taken courses through
            Wrightslaw Special Education Law and Advocacy Training Programs and
            I am currently earning a Certificate in the program at Wrightslaw--
            Understanding the Bell Curve -- Tests and Assessments. Currently, I
            am a member of Council of Parent Attorneys and Advocates (COPPA),
            Inc.
          </p>
          <p>
            My favorite pastimes are: photography, dancing and lip-syncing with
            my grand-daughter.
          </p>
        </div>
        <div>
          <img src="../assets/imgs/bio.jpg" alt="Marlena head shot" />
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>

<style lang="scss" scoped>
.bio {
  &-container {
    display: flex;
    align-content: center;
    justify-content: center;
    flex-wrap: wrap-reverse;
    background-color: white;
    min-height: 100%;
    padding: 20px 40px;
    width: 100%;

    @media only screen and (max-width: 550px) {
      padding: 20px 5px;
    }
  }

  &-content {
    width: 100%;
    margin-right: 20px;
    line-height: 1.5;
    padding-right: 15px;
    display: flex;
    justify-content: center;
    flex-wrap: wrap-reverse;

    @media only screen and (max-width: 800px) {
      justify-content: flex-start;
    }

    div {
      &:first-child {
        max-width: 700px;
        width: 100%;
        margin-right: 40px;

        @media only screen and (max-width: 800px) {
          margin-right: 0px;
          padding-left: 20px;
          width: 75%;
        }

        @media only screen and (max-width: 420px) {
          width: 100%;
        }
      }

      &:last-child {
        width: fit-content;

        img {
          margin-top: 20px;
          max-width: 450px;
          width: 100%;
          border-radius: 8px;
        }
      }
    }
  }

  &-imgContainer {
    display: flex;
    flex: 1;
    div {
      max-width: 500px;
      width: 100%;

      img {
        margin-top: 20px;
        max-width: 450px;
        width: 100%;
        border-radius: 8px;
      }
    }
  }
}
</style>
