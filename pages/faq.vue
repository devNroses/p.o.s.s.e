<template>
  <div>
    <Nav />
    <div class="faq-wrapper">
      <h2 class="pageTitle">Frequently Asked Questions:</h2>
      <div class="faq-content">
        <div>
          <h3>What is a Learning Challenge?</h3>
          <p>
            A learning challenge results from a difference in the way a child's
            brain is "wired" [Brain &#38; Life Magazine re Neurology Today].
            Children may have difficulty reading, writing, spelling, reasoning,
            recalling and/organizing information if left to figure things out by
            themselves or if taught in conventional ways.
          </p>
          <p>
            A learning challenge can be remediated with appropriate
            intervention, strategies and different types of remedial education;
            as: one-to-one tutoring; private tutoring, specialist tutoring, etc.
          </p>
        </div>

        <div>
          <h3>
            How Do You Know If Your Child Might Have a Learning Challenges?
          </h3>

          <p>
            It is often difficult based on observed behaviors to distinguish
            between slow learners and children with learning challenges. A child
            with learning challenges may have deficits in one or two areas while
            performing at or above the average standard in other areas. However
            it is often difficult, based on observed behaviors, to distinguish
            between slow learners and learning disabled persons. Basically a
            student with Learning Challenges have deficits in one or two areas
            while performing at or above the average in other areas. The child’s
            potential or overall intelligence is greater than his/her poor
            achievement would predict. This is called the ability-achievement
            discrepancy. It is possible for a child to have characteristics of
            both conditions.
          </p>
          <p>
            Actual diagnosis of a learning challenge can be diagnosed by a
            trained professional; clinical psychologists, educational
            psychologist and some physicians who are trained in this field.
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

          <p>
            According to the National Library of Medicine: "IQ is irrelevant to
            the definition of learning disabilities" In this article it was
            argued that IQ scores measure factual knowledge, expressive language
            abilities, and short-term memory, among other skills and that
            because children with learning disabilities have deficits in these
            areas, their scores may be spuriously low. It was also shown that
            some children with low IQ scores can be good readers, indicating
            that the low IQ scores does not necessarily result in poor reading.
            [Pub Med.Gov.]
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
