<template>
  <div>
    <Nav />
    <div class="faq-wrapper">
      <h2 class="pageTitle">Frequently Asked Questions:</h2>
      <div class="faq-content">
        <div>
          <h3>What is a Learning Challenges?</h3>
          <p>
            A learning challenges results from a difference in the way a
            person’s brain is “wired.” Children with learning challenges are as
            smart or smarter than their peers. But they may have difficulty
            reading, writing, spelling, reasoning, recalling and/organizing
            information if left to figure things out by themselves or if taught
            in conventional ways.
          </p>
          <p>
            A learning challenges can’t be cured or fixed, it is a lifelong
            issue. With the right support and intervention; however, children
            with learning challenges can succeed in school and go onto
            successful, often distinguished careers later in life.
          </p>
        </div>

        <div>
          <h3>
            How Do You Know If Your Child Might Have a Learning Challenges?
          </h3>

          <p>
            However it is often difficult, based on observed behaviors, to
            distinguish between slow learners and learning disabled persons.
            Basically a student with Learning Challenges have deficits in one or
            two areas while performing at or above the average in other areas.
            The child’s potential or overall intelligence is greater than
            his/her poor achievement would predict. This is called the
            ability-achievement discrepancy. It is even possible for someone to
            have characteristic of both conditions.
          </p>
          <p>
            Actual diagnosis of a learning challenges can only be done by a
            trained professional – clinical psychologists, educational
            psychologist, some physicians, etc.
          </p>
          <p>
            The last reference raises serious question about whether an
            ability-achievement discrepancy is a valid definition of a reading
            challenge. Well –replicated research has demonstrated that a core
            deficit for reading disabled individuals – both children and adults-
            is phonemic awareness (the ability to understand how sounds and
            sound patterns work in our language system).
          </p>
        </div>
        <div>
          <h3>How Common are Language-based Learning Challenges?</h3>
          <p>
            According to the International Dyslexia Association and Learning
            Challenges Association of American, about 15% of the population
            (close to one in seven) has a learning challenge. Of the students
            with learning challenges receiving special education services,
            70-80% have deficits in reading.
          </p>
        </div>

        <div>
          <h3>Does A Learning Challenge Mean You Have a Low IQ?</h3>
          <p>
            No. People with learning challenges are generally of average or
            above average intelligence and struggle in one or two areas where
            they need remedial educational help. Learning Challenges, by
            definition mean that a person’s skills in a particular area
            (reading, math visual/auditory processing, etc). are lower than
            would be expected by looking at the person’s overall IQ.
          </p>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>

<style lang="scss" scoped>
.faq {
  &-wrapper {
    background-color: white;
    padding: 25px;
    min-height: 70vh;
    display: flex;
    align-items: center;
    flex-direction: column;
  }

  &-content {
    display: flex;
    flex-wrap: wrap;
    align-content: center;
    align-items: center;
    justify-content: center;

    div {
      max-width: 75%;
    }
  }
}
</style>
