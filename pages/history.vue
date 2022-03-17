<template>
  <div>
    <Nav />
    <div class="about-container">
      <div class="about-history-wrapper">
        <h2 class="pageTitle">History</h2>
        <p>
          We are a 501 (c)(3) non-profit organization. P.O.S.S.E. began in 1998,
          when Marlena’s son, Michael, was diagnosed with a severe reading
          disability known as Dyseidetic, Dysphonetic Dyslexia. This is a
          learning challenge that affects children both visually and auditorily.
        </p>
        <p>
          Michael was in the second grade and was fortunate enough to have a
          teacher who noticed that he had special academic needs. The teacher
          admitted to not knowing the appropriate services to help him, but knew
          that it was imperative that he required academic help. Discouraged by
          lack of guidance from the school district and her son’s feelings of
          failure, she was left, through trial and error, to close the
          educational gap and make certain that the appropriate learning
          programs and remediation for her son’s needs were implemented.
        </p>
        <p>
          As a parent, she witnessed first-hand the agony, struggles and
          sleepless nights and days of “living” at his school to ensure that his
          educational needs were met. For more than a decade the family had
          struggled with academic challenges that seemed almost insurmountable
          at times. The maze they traveled for academic success resulted in a
          strong desire to make the road easier for other families in similar
          situations.
        </p>
        <p>
          P.O.S.S.E was birth from Michael's dream that no child should
          experience what he did. Every child deserves to enjoy their younger
          years at school and have the everlasting memories of success. Out of
          this P.O.S.S.E. was created.
        </p>
      </div>

      <div class="about-characterize">
        <h2 class="pageTitle">CHARACTERIZING LEARNING CHALLENGES</h2>
        <p>
          A Learning Disability does not define our children. It is a term used
          under I.D.E.A. [Individuals with Disabilities Education Act] With the
          appropriate support, intervention and remediation children with
          learning challenges will achieve success in school.
        </p>
        <p>
          Globally 1 in 7 of us live with a disability. And of those 80% are
          invisible. That is 1 Billion people who are living with a non-visible
          disability. While some of us experience a disability that is visible,
          many of us have a non-visible impairment or condition. [Journal of
          Sport Psychology in Action-Children.] In children, when we refer to a
          "Hidden Disabilities," a child that appears intelligent; however, the
          child is unable to demonstrate the skill level expected from a child
          of a similar age and grade level. Invisible Disabilities can be
          physical, mental or neurological conditions that can limit or
          challenge a child's movement, senses or activities and can impact
          their ability to learn. Our children can experience a combination of
          both visible and non-visible impairments and conditions.<br />
          "JUST BECAUSE YOU CAN'T SEE IT, DOESN'T MEAN THAT IT IS NOT THERE"
        </p>
        <p>
          Various learning challenges include: Dyscalculia affects a child's
          ability to understand numbers in math; Dysgraphia affects a child's
          handwriting ability and fine motor skills; Dyslexia affects reading
          and related language-based processing skills; Nonverbal learning
          challenges are when a child has trouble interpreting nonverbal cues
          such as a facial expression or body language and may have poor
          coordination; Oral/Written Language Disorder and Specific Reading
          Comprehension Deficit affects a child's understanding of what they are
          reading or of spoken language. Dyspraxia is a neurological (or
          brain-based) disorder that impacts a child’s ability relating to gross
          motor skills, motor planning and coordination.
        </p>
        <p>
          Attention-Deficit/Hyperactivity Disorder (ADHD) is a brain disorder.
          Scientists have shown that there are differences in the brains of
          children with ADHD and some of these differences change as a child
          ages and matures. The front of the brain behind the forehead is the
          frontal lobe. The frontal lobe is the part of the brain that helps
          children to organize, plan, pay attention, and make decisions. Parts
          of the frontal lobe may mature a few years later in children with
          ADHD. The frontal lobe is the area of the brain responsible for:
          Problem Solving; Memory; Language; Motivation; Judgment; Impulse
          Control; Social Behavior; Planning; Decision-making; Attention;
          Ability to delay Gratification and Time Perception [American Academy
          of Child &amp; Adolescent Psychiatry].
        </p>
        <p>
          Executive Functions are the cognitive abilities needed to control our
          thoughts, emotions and actions. How does this relate to children? The
          phrase "Executive Function" refers to a set of skills. These skills
          underlie the capacity to plan ahead and meet goals, display
          self-control, follow multiple-step directions even when interrupted,
          and stay focused despite distractions, among others. These skills
          typically develop most rapidly between ages 3-5, followed by another
          spike in development during the adolescent and early adult years. It
          takes a long time and a lot of practice to develop them, but,
          children's executive function skills grow, adults can gradually allow
          children to manage more and more aspects of their environment. Key:
          The increasingly competent executive functioning of children and
          adolescents enables them to plan and act in a way that makes them good
          students, classroom citizens and friends [Center on the Developing
          Child Harvard University].<br />
          "BUILDING CHILDREN'S EXECUTIVE FUNCTION SKILLS BENEFITS EVERYONE."
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
    padding-left: 15px;
    padding-right: 40px;
    display: flex;
    flex-direction: column;
    align-items: center;

    @media only screen and (max-width: 400px) {
      padding-right: 20px;
    }
    h2 {
      text-align: center !important;
    }
  }

  &-intro {
    &-container {
      display: flex;
      justify-self: center;
      align-self: center;
      width: 80%;
      margin: 0 auto;
      max-width: 1200px;
      text-align: left !important;
    }

    &-content {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
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
      width: 85%;
      display: flex;
      flex-wrap: wrap;
      padding: 15px;
      justify-content: center;
      margin-top: -15px;

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

    p {
      max-width: 1050px;
      line-height: 1.25;
      text-align: left;
    }
  }
}
</style>
