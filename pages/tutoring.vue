<template>
  <div>
    <Nav />
    <div class="tutoring-container">
      <div class="tutoring-info">
        <p>
          Below are a list of avialable tutors that will help your child during
          their educational journey. If you have any interest please reach out
          to the tutor directly through the provided contact routes available.
        </p>
      </div>
      <div class="tutor-wrapper">
        <img src="~/assets/imgs/dennis_squier.jpg" alt="Dennis Squier" />
        <p class="tutor-title">
          DENNIS SQUIER
        </p>
        <p class="tutor-subject">
          <b>Math</b><br />
          <i
            >Algebra, Geometry, Trigonometry, and Pre-Calculus (Grade 4 through
            College)</i
          >
        </p>
        <p class="tutor-subject">
          <b> Science</b><br />
          <i>General Science (Grade 4 through Middle School)</i>
        </p>

        <div class="tutor-about">
          <p class="tutor-rates-header">About</p>
          Dennis Squier received a Bachelor of Arts Degree with Distinction in
          Mathematics in 1967. Throughout his college expereince, Dennis was
          tutoring gained experience tutoring in Math and Science. After collge
          he worked for 40 years as a Software Engineer for the U.S. Navy. Along
          with working in software enginnering, Dennis ended up teaching
          software enginnering subjects throughout his career. During 2008 -
          2010 school year, Dennis tutored for the following subjects,
          Pre-calculus, Geometry and Algebra to students.
        </div>

        <div class="tutor-rates">
          <p class="tutor-rates-header">Rates</p>
          <p class="tutor-rates-price">First hour: <span>$40</span></p>
          <p class="tutor-rates-price">
            Subsequent hours (per hour): <span>$30</span>
          </p>
        </div>
        <div class="tutor-contact">
          <a href="mailto:dennis@possesandiego.org">Email</a>
          <a href="tel:6196984685">Call</a>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>

<style lang="scss" scoped>
.tutoring {
  &-container {
    background: white;
    padding: 25px;
  }

  &-info {
    margin-bottom: 40px;
    p {
      font-size: 16px;
      font-weight: 600;
      font-style: italic;
      line-height: 1.5;
    }
  }
}

.tutor {
  &-wrapper {
    border: 1px solid #383f34;
    border-radius: 10px;
    padding: 15px;
    height: 100%;
    max-width: 500px;
    line-height: 1;
  }

  &-title {
    font-size: 24px;
    font-weight: 700;
    margin-bottom: -4px;
  }

  &-subject {
    font-size: 16px;
  }

  &-about {
    margin: 15px auto;
    font-size: 18px;
    line-height: 1.5;
  }

  &-rates {
    width: 100%;
    display: flex;
    flex-direction: column;
    margin-bottom: 10px;

    p {
      line-height: 0.25;
    }

    &-header {
      font-size: 18px;
      font-weight: 700;
      color: #383f34;
      padding-bottom: 15px;
      border-bottom: 1px solid lightgrey;
    }

    &-price {
      span {
        font-weight: bold;
        font-size: 20px;
      }
    }
  }

  &-contact {
    display: flex;
    justify-content: space-evenly;
    flex-wrap: wrap;

    a {
      width: 200px;
      padding: 20px;
      background: #383f34;
      color: white;
      font-size: 16px;
      font-weight: 600;
      text-align: center;
      border-radius: 8px;
      margin: 10px auto;

      &:hover {
        cursor: pointer;
        color: #383f34;
        background: white;
        border: 1px solid #383f34;
      }
    }
  }
}
</style>
