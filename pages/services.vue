<template>
  <div>
    <Nav />
    <PaySummary
      :purchaseList="shoppingCart"
      :cartTotal="finalTotal"
      :removeItem="(e) => updatePurchaseList(e)"
    />
    <div class="services-wrapper">
      <div class="services-intro">
        <h2 class="pageTitle">P.O.S.S.E. Services</h2>
      </div>
      <div class="levelUp-wrapper" v-for="(service, i) of services" :key="i">
        <div class="levelUp-price">
          <div>
            <h3 class="levelUp-name">{{ service.name }}</h3>
            <p class="price">{{ `$${service.price}.00` }}</p>
          </div>
          <button
            :style="[hasItem(service) ? { backgroundColor: '#373F34' } : '']"
            v-on:click="updatePurchaseList(service)"
            class="purchaseButton"
          >
            {{ hasItem(service) ? "Remove service" : "Purchase service" }}
          </button>
        </div>

        <p>
          {{ service.details }}
        </p>
        <h4>Anticipated/Expected Outcome:</h4>
        <p>
          {{ service.anticipatedDetails }}
        </p>
      </div>
    </div>

    <Footer />
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import PaySummary from "../components/PaySummary.vue";
export default Vue.extend({
  components: {
    PaySummary,
  },
  data() {
    return {
      services: [
        {
          name: "Level I: Consultation Phase",
          price: "75",
          details: `One hour Conference with Parent(s) to discuss in detail the child's educational background and performance through grade level. This will enable P.O.S.S.E. to fully understand the child's learning challenges and how this is affecting their productivity within the classroom setting and will be shared with parents.  We will discuss what an IEP should include. We will discuss the Referral, Identification and Eligibility of the child and role of Parents in the IEP Process.`,
          anticipatedDetails: `Parents are familiarized with the IEP Process and can begin to understand the in-depth process of their child's educational needs and how this is affecting their productivity within the classroom setting presently. Parents are able to make an informed decision if our program is appropriate in assisting with their child's needs.`,
        },
        {
          name: "Level II: Critical Assessment Phase",
          price: "375",
          details: `Obtain All Initial Assessments that have already been administered to the child by the School. Obtain all school records including all IEPs. Prepare Written Plan of Action within our program for Parent(s) to include the following: Present Levels of Performance (PLOP). This PLOP will include the Annual Goals, Benchmarks, Measuring and Reporting Progress that can be determined after records review and incorporated in the Plan of Action. Determine any unique needs that the child may have that are not identified by the school or on the IEP.  Determine what services the school has implemented to address each need; what will the child be able to accomplish as a result of the services that the school has placed on the IEP. This is critical because P.O.S.S.E. can determine if the child is receiving a FAPE. Detailed correspondence to School Principal/District to obtain ALL records, tests, assessments, protocols and IEPs through grade level from all schools of child's attendance.`,
          anticipatedDetails: `Parents will be able to determine from this session whether the services on the IEP are projecting that the child is making Measurable Educational gains as provided under IDEA. Parents can determine after receiving their Written Plan of Action if our program is appropriate for their child and they wish to retain services of P.O.S.S.E. to assist. 
`,
        },
        {
          name: "Level III: P.O.S.S.E. Parent Notebook and Parent Training",
          price: "1800",
          details: `Parent will receive Working IEP Notebook with all of child's records in Chronological Order with preparation worksheets for upcoming IEP meetings.  Parents will be trained via Zoom or in person if possible (COVID) regarding preparing for IEP meetings.  The training will entail the use of the binder and how to advocate using the school records and reports for services for their child.  Parents will be provided with all reports or assessments that have been given by school at least three days before the IEP meeting and will be reviewed by P.O.S.S.E. and parent in preparation for the meeting. Pre-IEP meetings will take place via Zoom with Parent. An outline will be provided to Parent for upcoming IEP meeting with Parent's concerns to be discussed at meeting. P.O.S.S.E. will continue with development of the IEP and drafts until the IEP addresses SMART GOALS: Specific, Measurable, Achievable, Realistic and Time-Bound. It can take up to one year to work with the Parent and school district.  Parent training continually throughout this phase of the program. P.O.S.S.E. will be present with Parent either Zoom or in person at the IEP meetings through the duration of the preparation of the IEP for the child.`,
          anticipatedDetails: `Parents through the program are now thoroughly trained and equipped with the understanding of how the special education system works and are able to advocate for their child.  Parents will have skill sets as an advocator to communicate effectively and in collaboration with the school and maintain a professional relationship. Parents will know the right questions to ask. Parents will be prepared, organized and ready to attend the meetings. Parents will be able to express their child's needs in a clear and concise manner. Parents will learn how to communicate effectively with teachers and other school personnel to create an effective learning environment for their child and to ensure that their child's school is providing the services or programs that he or she needs to succeed in school. Parents will be empowered with knowing their rights as a Parent.`,
        },
        {
          name: "Level IV: Prepare Detailed Timeline Chart of Child's Educational Records",
          price: "3800",
          details: `Parents are now proficient in the IEP Process and can continue on their own to be effective advocates for their child.  Certificate of Completion as having acquired the skill set level of an effective advocator for their child.  Parents have the opportunity to pay a membership fee for continued services for P.O.S.S.E. to assist with all future IEP's for their child through 12th grade and assistance with College Preparatory Services with P.O.S.S.E.'s affiliate company.  Services of all above. Continued Training with P.O.S.S.E and Parent in advocacy skills for their child's IEP services; Classroom observations if applicable; Visits for on campus sites regarding appropriate placement per the goals and objectives on the IEP.  Attendance at all IEP Meetings (Zoom or in person); P.O.S.S.E. takes Notes from IEP Meetings for Parents to add as an Addendum to meeting Notes; Review Draft IEP with Parents and continue until Final IEP is in place for the child.  Assistance with Transitional services for child if appropriate; Assistance with Extended School Year.  Assistance with preparing Transition Assessments for future preparation for getting a job, college or living independently. Assistance with Transition Assessments is a step to helping your child set goals in the future. Parents will be provided a USB data entry stick to enter data on their Child's Timeline Chart and training on data entry.  P.O.S.S.E. will assist and attend for Mediation Sessions with Parent.`,
          anticipatedDetails: `Parents are now trained to be an effective advocate for their child
          until graduation and can determine if services provided by the school
          are meeting the child’s needs and is the school providing a FAPE [Free
          Appropriate Public Education].`,
        },
      ],
      shoppingCart: [],
      finalTotal: 0,
    };
  },
  methods: {
    updatePurchaseList(item) {
      const resutOfCheck = this.hasItem(item);
      if (resutOfCheck) {
        this.shoppingCart = this.shoppingCart.filter(
          (el) => el.name !== item.name
        );
      } else {
        this.shoppingCart.push(item);
      }
      this.totalValue();
    },
    hasItem(checkItem) {
      return this.shoppingCart.some((item) => item.name === checkItem.name);
    },
    totalValue() {
      let total = 0;
      if (this.shoppingCart.length) {
        for (let item of this.shoppingCart) {
          total = total + parseInt(item.price);
          this.finalTotal = total;
        }
      }
    },
  },
});
</script>

<style lang="scss" scoped>
.services {
  &-wrapper {
    display: flex;
    padding: 25px;
    flex-direction: column;
    background-color: white;
  }

  &-intro {
    display: flex;
    flex-direction: column;
    margin: 0 auto 25px;
    justify-content: center;
    align-items: center;
    max-width: 800px;
    text-align: center;

    h3 {
      margin-bottom: 5px;
    }
  }

  &-title {
    font-size: 30px;
    text-align: left;
  }
  &-list {
    display: flex;
    justify-content: space-evenly;
    flex-wrap: wrap;
  }
  &-profile {
    border: 1px solid #849c7a;
    width: 250px;
    border-radius: 8px;
    padding: 15px;
    margin: 10px 0px;
    padding-bottom: 20px;
    text-align: center;

    h3 {
      color: #383f34;
      font-size: 22px;
    }
  }
}

.service {
  &-position {
    font-family: Arial, Helvetica, sans-serif;
    font-size: 15px;
    color: gray;
  }

  &-address {
    font-size: 18px;
    font-weight: 600;
    margin-top: 8px;
    line-height: 1.25;
    margin-bottom: 10px;
    color: #849c7a;
  }

  &-phone,
  &-email,
  &-website {
    margin: 15px auto;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    a {
      border: 1px solid #e4f0d8;
      border-radius: 10px;
      background: #849c7a;
      color: white;
      padding: 8px 30px;
      margin: 8px;
    }
  }

  &-email {
    margin-bottom: 0px;
  }

  &-list {
    display: flex;
    justify-content: space-evenly;
    flex-wrap: wrap;
    margin-bottom: 30px;
    div {
      border: 1px solid #849c7a;
      background: #849c7a;
      color: white;
      font-size: 16px;
      border-radius: 10px;
      width: 200px;
      margin: 10px;
      padding: 25px;
      text-align: center;
      min-height: 100px;
      display: flex;
      justify-content: center;
      align-content: center;
      align-items: center;
    }
  }
}

.levelUp {
  &-wrapper {
    width: 100%;
    display: flex;
    flex-direction: column;
    max-width: 1200px;
    justify-self: center;
    margin: 0 auto 20px;

    h4 {
      margin-top: -5px;
      margin-bottom: -10px;
    }
  }
  &-purchase {
    display: flex;
    align-items: flex-end;
    margin-bottom: 15px;
    margin-top: -15px;

    button {
      background-color: #669139;
      border-radius: 8px;
      border: none;
      color: white;
      font-size: 14px;
      font-weight: 600;
      height: 40px;
      margin-right: 30px;
      margin-bottom: 18px;
      padding: 8px 16px;
      cursor: pointer;

      &:hover {
        background-color: #d5b9b2 !important;
      }
    }

    h3 {
      padding: 8px 16px;
    }
  }

  &-price {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    border-bottom: 1px solid gray;
    margin-bottom: 5px;
  }

  &-name {
    min-width: 380px;
    max-width: 580px;
  }
}

.price {
  color: #849c7a;
  font-size: 24px;
  font-weight: bold;
  font-family: Arial, Helvetica, sans-serif;
  margin: -10px 0 10px;
}

.purchaseButton {
  background-color: #669139;
  border-radius: 6px;
  color: white;
  cursor: pointer;
  font-size: 16px;
  height: 30px;
  margin-top: 12px;
  padding: 5px 16px;
  border: 1px transparent;

  &:hover {
    background-color: #849c7a;
  }
}
</style>
