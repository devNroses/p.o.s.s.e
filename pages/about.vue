<template>
  <div>
    <Nav />
    <div class="about-container">
      <div class="about-intro-container">
        <div class="about-intro-content">
          <div>
            <h1>Parents of Students in Special Education</h1>
            <p>
              P.O.S.S.E is an independent, nonprofit, §501(c)(3) tax-exempt
              organization of parents, educational professionals, doctors,
              attorneys and, special educational advocates.
            </p>
          </div>
          <div class="about-icon">
            <img src="~/assets/imgs/aboutIcon.svg" alt="about icon" />
          </div>
        </div>
      </div>

      <div class="about-history-wrapper">
        <div>
          <h3>Start Journey</h3>
          <p>
            Parents of Students in Special Education (P.O.S.S.E., Inc.) is an
            independent, nonprofit, §501(c)(3) tax-exempt organization of
            parents, educational professionals, doctors, attorneys and, special
            educational advocates. P.O.S.S.E. began in 1998, when Marlena’s son,
            Michael, was diagnosed with a severe reading disability known as
            Dyseidetic, Dysphonetic Dyslexia. This is a learning disability that
            affects children both visually and auditorily.<br />
            Michael was in the second grade and was fortunate enough to have a
            teacher who noticed that he had special academic needs. The teacher
            admitted to not knowing the appropriate services to help him, but
            knew that it was imperative that he required academic help.
          </p>
        </div>
        <div>
          <h3>Signs of Struggle</h3>
          <p>
            Discouraged by lack of guidance from the school district and her
            son’s feelings of failure, she was left, through trial and error, to
            close the education gap and make certain that the appropriate
            learning programs and remediation for her son’s needs were
            implemented. After four years of setbacks her 19-year-old son is
            reading at grade level and graduated with his class on June 14, 2008
            and is attending Grossmont College. He is preparing to enter Berklee
            School of Music in Boston.<br /><br />
            She witnessed first-hand the agony, struggles and sleepless nights
            and days of “living” at his school to ensure that his educational
            needs were met. For more than a decade the family had struggled with
            academic challenges that seemed almost insurmountable at times.
          </p>
        </div>
        <div>
          <h3>Beinging of P.O.S.S.E</h3>
          <p>
            The maze they traveled for academic success resulted in a strong
            desire to make the road easier for other families in similar
            situations. Michael’s dream was to fulfill that no child had to
            experience what he did and that every child deserves to enjoy their
            younger years at school and have that everlasting memory of history
            to pass onto their children and Michael wanted me to put this in
            motion -- Thus, P.O.S.S.E was formed.
          </p>
        </div>
      </div>

      <div class="about-characterize">
        <h2>CHARACTERIZING LEARNING DISABILITES</h2>
        <p>
          Learning disabilities in school children are characterized by a
          significant difference in achievement as compared to his or her
          overall intelligence. While quite normal, even above average or
          exceptional in many respects, children with learning disabilities tend
          to interpret differently what they see or hear. They are often
          oriented differently to relationships in space and time, and may show
          poor coordination, lapses of memory, and disorganized thinking.
          Although neurological tests, as a rule, show no abnormalities, these
          children are often far behind their age peers in reading, spelling,
          writing, and math.
        </p>

        <p>
          Children whose educational needs are not being met often experience
          lives of frustration, confusion, and unwarranted failure. Many reach a
          point of being dysfunctional in a traditional classroom or special
          education program. They are often angry at the system, for it seems
          they fail no matter how hard they try. Some give up and just stop
          working. Without appropriate educational intervention, the prospects
          are very slim for children with learning disabilities successfully
          completing school and living fulfilling lives as productive citizens.
        </p>

        <p>
          The bitter irony is that, despite the inability of these children to
          perform well in conventional school programs, they are typically
          neither lazy nor not intelligent. In fact, they are often quite
          bright, gifted with unique talents, and very eager to learn. The
          problem is not that they are unable to learn traditional school and
          social skills, but that they can't learn them in the traditional way.
        </p>
      </div>
    </div>
    <Footer />
  </div>
</template>

<style lang="scss" scoped>
.about {
  &-container {
    background-color: white;
    min-height: 100%;
    padding: 25px;
  }

  &-intro {
    &-container {
      display: flex;
      justify-self: center;
      align-items: center;
      align-self: center;
      width: 80%;
      margin: 0 auto;
      max-width: 1200px;
    }

    &-content {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-evenly;
      width: 100%;

      div {
        &:first-child {
          max-width: 760px;
          h1 {
            font-size: 36px;
          }

          p {
            width: 85%;
            font-size: 18px;
            text-transform: uppercase;
            font-weight: 200;
            line-height: 1.5;
          }
        }
      }
    }
  }

  &-icon {
    display: flex;
    justify-content: center;
    align-items: center;
    align-content: center;
    padding: 0 50px;

    img {
      width: 240px;
    }
  }

  &-history {
    &-wrapper {
      width: 100%;
      display: flex;
      justify-content: space-evenly;
      flex-wrap: wrap;
      padding: 15px;
      margin: 0 -20px;

      div {
        width: 380px;
        height: 320px;
        display: flex;
        padding: 20px;
        text-align: left;
        border: 1px solid #ccc;
        border-radius: 10px;
        flex-direction: column;
        margin: 10px auto;

        @media only screen and (max-width: 500px) {
          height: auto !important;
        }

        h3 {
          margin: -10px auto -5px;
          font-size: 28px;
          font-weight: bold;
          color: #849c7a;
        }

        p {
          line-height: 1.2;
        }
      }
    }
  }

  &-characterize {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-content: center;
    align-items: center;

    p {
      max-width: 700px;
      line-height: 1.25;
      text-align: center;
    }
  }
}
</style>
