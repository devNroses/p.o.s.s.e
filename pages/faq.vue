<template>
  <div>
    <Nav />
    <div class="faq-wrapper">
      <h1>Frequently asked questions:</h1>
      <div class="faq-content">
        <div class="faq-question">
          <a
            v-for="faq in faqs"
            :key="faq.id"
            @click="setQuestionIndex(faq.id)"
            class="faq-title"
            :aria-label="'Review ' + faq.question"
          >
            {{ faq.question }}
          </a>
        </div>

        <div class="faq-answers">
          <div v-for="faq in faqs" :key="faq.id">
            <div v-show="showByIndex === faq.id">
              <h3>{{ faq.question }}</h3>
              <h3>Answer:</h3>
              <p>
                {{ faq.answer }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  data() {
    const faqs: any[] = [
      {
        id: 1,
        question: "What is a Learning Disability?",
        answer: `A learning disability results from a difference in the way a
            person’s brain is “wired.” Children with learning disabilities are
            as smart or smarter than their peers. But they may have difficulty
            reading, writing, spelling, reasoning, recalling and/organizing
            information if left to figure things out by themselves or if taught
            in conventional ways. A learning disability can’t be cured or fixed,
            it is a lifelong issue. With the right support and intervention;
            however, children with learning disabilities can succeed in school
            and go onto successful, often distinguished careers later in life.`
      },
      {
        id: 2,
        question:
          "How Do You Know If Your Child Might Have a Learning Disability?",
        answer: `According to government regulations, students with learning disabilities have “disorders in one or more basic psychological processes involved in understanding or using language, spoken or written which may manifest itself in an imperfect ability to listen, think, speak, read, write, spell or do mathematical calculations.”
However it is often difficult, based on observed behaviors, to distinguish between slow learners and learning disabled persons.  Basically a student with Learning Disabilities have deficits in one or two  areas while performing at or above the average in other areas. The child’s potential or overall intelligence is greater than his/her poor achievement would predict. This is called the ability-achievement discrepancy.  It is even possible for someone to have characteristic of both conditions.
Actual diagnosis of a learning disability can only be done by a trained professional – clinical psychologists, educational psychologist, some physicians, etc. 
The last reference raises serious question about whether an ability-achievement discrepancy is a valid definition of a reading disability.  Well –replicated research has demonstrated that a core deficit for reading disabled individuals  – both children and adults- is phonemic awareness (the ability to understand how sounds and sound patterns work in our language system).
`
      },
      {
        id: 3,
        question: "How Common are Language-based Learning Disabilities?",
        answer: `According to the International Dyslexia Association and Learning Disability Association of American, about 15% of the population (close to one in seven) has a learning disability.  Of the students with learning disabilities receiving special education services, 70-80% have deficits in reading.`
      },
      {
        id: 4,
        question:
          "Does A Learning Disability Mean You Have  a Low IQ?What is a Learning Disability?",
        answer: `No.  People with learning disabilities are generally of average or above average intelligence and struggle in one or two areas where they need remedial educational help.  Learning Disabilities, by definition mean that a person’s skills in a particular area (reading, math visual/auditory processing, etc). are lower than would be expected by looking at the person’s overall IQ.`
      }
    ];
    return {
      faqs,
      showByIndex: 1
    };
  },
  methods: {
    setQuestionIndex(id: any) {
      this.showByIndex = id;
    }
  }
});
</script>
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
  }

  &-question {
    padding: 15px;
    display: flex;
    flex-direction: column;
    width: 100%;
    max-width: 800px;
    min-width: 325px;

    a {
      font-size: 32px;
      font-weight: 400;
      margin: 15px;
      cursor: pointer !important;
      margin: 25px 0px;
      transition: color 0.5s ease-in-out;

      &:hover {
        cursor: pointer;
        color: #e4f0d8;
      }
    }
  }

  &-answers {
    flex: 1;
    padding: 15px;
    display: flex;
    flex-direction: column;
    border: 1px solid #ccc;
    border-radius: 8px;

    p {
      font-size: 20px;
      line-height: 1.25;
      font-weight: 300;
    }
  }
}
</style>
