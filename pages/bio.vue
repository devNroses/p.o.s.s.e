<template>
  <div>
    <Nav />
    <div class="bio-container">
      <div class="bio-content">
        <div>
          <h2 class="pageTitle">Bio</h2>
          <p>
            A native of San Diego, Marlena, fell in love with doing charitable
            work for children through her various commitments to different
            organizations. She loves reading and discovered the wonderful world
            of books at a young age. Through reading, she wanted to change a
            child's world. Her love for reading and reading to children made her
            realize how important it is for children to be able to read. She
            realized her deep appreciation for how non-profits can seek to
            improve the quality of education for children and her continued
            passion for charitable work lead her to want to make a difference in
            a child's life. This passion developed even further when her son was
            diagnosed with Dyslexia.
          </p>
          <p>
            Marlena loves to read five books at any given time depending on what
            mood she is in for reading on that day. (Smile) She has been a
            paralegal for 40 years working continuously in the legal field. She
            began educating herself when she had to advocate for her son and the
            insurmountable educational obstacles she had to overcome so that her
            son would be able to read. She changed to Special Education Law and
            became an Advocate working with Parents and their children for 15
            years assisting parents to be able to find their voice and have a
            seat at the IEP Meetings with knowledge and understanding in their
            child's educational journey through the Individual Educational
            Program (IEP). She graduated with a Certificate from the William and
            Mary Law School Advocacy Program( lifetime Member of ISEA Alumni
            Group) and continued her education with a Certificate from the
            University of San Diego Law School Special Education Advocacy
            Program. She is a member of Wright Law and is currently earning her
            Certificate in the program at Wrights Law for the Bell Curve Reading
            Tests and Assessments. She is a member of the Council of Parent
            Attorneys and Advocates (COPAA), Inc. Her favorite pastime is
            photography, dancing, and lip singing with her granddaughter.
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
