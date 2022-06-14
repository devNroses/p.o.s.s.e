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
        <h2 class="pageTitle">Coaching Services</h2>
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
        <h4>Instructions on How to Obtain Services</h4>
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
          name: "Level I: Comprehensive Consultation  (75 minutes)",
          price: "275",
          details: `A comprehensive review of your child's records: to include last two IEP's, evaluations from private or public assessments, work samples and progress reports.  We will discuss what an IEP should include, the referral process, eligibility and role of Parents in the IEP Process. We will follow-up with a one hour virtual live coaching session to review the findings and outline a game plan. By the end of this session, you will have the tools necessary to advocate for your child at their present grade level.`,
          anticipatedDetails: `If you have selected this Level of Service, please email me at: 
marlena@possesandiego.org. In your email please include: Full Name, Address and Telephone Number; Child's Full Name; Grade level and School of Attendance. Please also include a brief description (no more than three paragraphs) what you feel is challenging for your child and their performance levels as you have observed so we can discuss in consultation/coaching session.  Please expect a 12 hour response time to set up either a Zoom meeting or in-office visit.`,
        },
        {
          name: "Level II: General Special Education Advocacy Services",
          price: "575",
          details: `Up to 5 hours; Note if records are voluminous an additional fee may be required. 
          We prepare  detailed correspondence to School Principal/District to obtain ALL records, tests, assessments, protocols and IEP's from all schools of your child's attendance. P.O.S.S.E will prepare a Written Plan of Action based on your child's file and records received to date; including the following: Determine where child is currently performing from their Present Levels of Performance (PLOP) according to the IEP. This PLOP will include the Annual Goals, Benchmarks, Measuring and Reporting Progress that can be determined after records review and incorporated in the Plan of Action. Determine any unique needs that the child may have that are not identified by the school or on the IEP. Determine what services the school has implemented to address each need; what will the child be able to accomplish as a result of the services that the school has placed on the IEP to determine if child is receiving a FAPE.`,
          anticipatedDetails: `If you have selected this Level of Service, please email me at:
marlena@possesandiego.org  Please include in your email dates and times that you are available to set up our Second Meeting and Review P.O.S.S.E.'s Written Plan of Action. Parent can take their Written Plan of Action and be prepared to address your  child's concerns, to effectively advocate for your child's needs. This can be an office visit, Zoom or Conference Call. 
Level III: Targeted Special Education Advocacy Services $1500.00 up to six months of service: We provide eight parent Zoom training sessions in advocacy pertaining to your child's IEP. Parents will receive a P.O.S.S.E. IEP Tote Kit with parent notebook including worksheets for the entire school year. Pre-IEP Parent preparation for meetings. We will provide 6 months of service monitoring emails and providing resources to understand your rights and attending IEP meetings. We will fully prepare parents for each IEP meeting throughout the term of our services.
Instructions on How to Obtain Services 
If you have selected this Level of Service, please email me at 
marlena@possesandiego.org. We will respond in 12 hours and advise our next steps. 
`,
        },
        {
          name: "Level III: P.O.S.S.E. Parent Notebook and Parent Training",
          price: "1800",
          details: `Parent will receive Working IEP Notebook with all of child's records in Chronological Order with preparation worksheets for upcoming IEP meetings.  Parents will be trained via Zoom or in person if possible (COVID) regarding preparing for IEP meetings.  The training will entail the use of the binder and how to advocate using the school records and reports for services for their child.  Parents will be provided with all reports or assessments that have been given by school at least three days before the IEP meeting and will be reviewed by P.O.S.S.E. and parent in preparation for the meeting. Pre-IEP meetings will take place via Zoom with Parent. An outline will be provided to Parent for upcoming IEP meeting with Parent's concerns to be discussed at meeting. P.O.S.S.E. will continue with development of the IEP and drafts until the IEP addresses SMART GOALS: Specific, Measurable, Achievable, Realistic and Time-Bound. It can take up to one year to work with the Parent and school district.  Parent training continually throughout this phase of the program. P.O.S.S.E. will be present with Parent either Zoom or in person at the IEP meetings through the duration of the preparation of the IEP for the child.`,
          anticipatedDetails: `Parents through the program are now thoroughly trained and equipped with the understanding of how the special education system works and are able to advocate for their child.  Parents will have skill sets as an advocator to communicate effectively and in collaboration with the school and maintain a professional relationship. Parents will know the right questions to ask. Parents will be prepared, organized and ready to attend the meetings. Parents will be able to express their child's needs in a clear and concise manner. Parents will learn how to communicate effectively with teachers and other school personnel to create an effective learning environment for their child and to ensure that their child's school is providing the services or programs that he or she needs to succeed in school. Parents will be empowered with knowing their rights as a Parent.`,
        },
        {
          name: "Level IV: Full School Year Special Education (10 month school year)",
          price: "3800",
          details: `We will provide special education advocacy services for the entire school year. P.O.S.S.E. personally advocates for your child includes all Levels of Services addressed above.  This includes attending all IEP Meetings with parent; parent preparation for IEP meetings with Parent Checklist/Concerns. Review emails and responses. Includes assistance with Extended School Year services. Classroom observations, if applicable; Visits for on campus sites regarding appropriate placement per the goals and objectives on the IEP.  P.O.S.S.E. takes Notes from IEP Meetings for Parents to add as an Addendum to meeting Notes; Review Draft IEP with Parents and continue until Final IEP is in place for your child with Placement. Assistance with Transitional services for child if appropriate. Prepare for and attend Transition Assessment and attendance at Transition IEP meeting. Parent will receive Child's Individualized Timeline of entire school records for advocacy tool and will be trained on how to use and keep Timeline current for your child's educational journey. By the end of this package parents will be able to advocate for the upcoming school years on their own. This service does not exceed 10 months.  If additional coaching sessions are needed an additional $100.00 per hour is required.`,
          anticipatedDetails: `If you have selected this Level of Service, please email me at:
marlena@possesandiego.org.  Your email will be answered within 12 hours and we will send you what is needed, signed authorizations for P.O.S.S.E.`,
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
    flex-direction: column;
    background-color: white;
    padding-left: 40px;
    padding-right: 40px;
    @media only screen and (max-width: 390px) {
      padding-right: 20px;
    }
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
    font-weight: 600;
  }
}

.price {
  color: #383f34;
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
  margin-bottom: 12px;
  padding: 5px 16px;
  border: 1px transparent;

  &:hover {
    background-color: #849c7a;
  }
}
</style>
