<template>
  <div>
    <Nav />
    <PaySummary :purchaseList="shoppingCart" />
    <div class="services-wrapper">
      <div class="services-intro">
        <h2 class="pageTitle">P.O.S.S.E. Services</h2>
      </div>
      <div class="levelUp-wrapper" v-for="(service, i) of services" :key="i">
        <div class="levelUp-price">
          <h3 class="levelUp-name">{{ service.name }}</h3>

          <div class="levelUp-purchase">
            <button>Buy Service</button>
            <h3>{{ service.price }}</h3>
          </div>
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
export default Vue.extend({
  data() {
    return {
      services: [
        {
          name: "Level I: Consultation Phase",
          price: "$75.00",
          details: ` Conference with Parent(s) to discuss the overall performance of the
          child's educational background through their grade level. This will
          enable P.O.S.S.E. to fully understand the child's learning challenges
          and how this is affecting their productivity within the classroom
          setting. Discuss how the child qualified i.e.”Eligibility” for
          services. Discuss Parent’s role at their child’s IEP meeting; Discuss
          what Parents should expect in an IEP Meeting; Who should attend their
          child’s IEP meeting with relation to their child’s teachers.`,
          anticipatedDetails: `Parents become familiar and can begin to understand the in depth
          process of their child’s educational needs and begin to understand the
          IEP Process as it pertains to their child.`,
        },
        {
          name: "Level II: Critical Assessment Phase",
          price: "$375.00",
          details: `Initial Assessment of what tests have been given and if the school has
          done a thorough evaluation in all areas of suspected disability for
          the child. Review records Parents have from the school. Prepare detail
          written correspondence to School Prinicipal/District to obtain ALL
          records, tests, assessments and protocols through grade level from all
          schools of child’s attendance. Determine based on school records
          whether child is performing at grade level or below grade level.
          Review Present levels of Performance (PLOP). Determine any unique
          needs that the child may have that are not identified by the school or
          on the IEP; Determine what services the school has implemented to
          address each need; what will the child be able to accomplish as a
          result of the services. Review all IEP Goals and Objectives on the
          current IEP and fomer IEPs; Advice of additional assessments for the
          child.`,
          anticipatedDetails: `Parents will be able to make an informed decision as to where the
          child is performing grade level and if the child has made measurable
          educational gains as provided under IDEA.`,
        },
        {
          name: "Level III: P.O.S.S.E. Parent Notebook and Parent Training",
          price: "$1,075.00",
          details: `Parent receives notebook with all of child’s records in Chronological
          order with worksheet and progress sheets for upcoming IEP meetings,
          begin parent training with P.O.S.S.E. until completion of IEP process;
          preparation of Parent Agenda for Meetings; Review and discuss all
          Evaluation assessments that were given to child; Review and make sure
          Parents have all reports three days before the IEP Meeting to discuss
          at meeting; Pre-IEP meeting with Parent to address concerns;
          attendance at two IEP Meetings (Via Zoom) or in person if applicable;
          Recording of IEP Notices given.`,
          anticipatedDetails: `Parents have completed the training program and will have the
          knowledge and understanding to continue to plan for their child's
          educational needs as the child progresses through each grade level.
          Parents are prepared to begin advocating for their child and
          understand what has to be provided by the school under IDEA and what
          their child is entitled to under the law on their child’s Independent
          Educational Plan.`,
        },
        {
          name: "Level IV: Timeline Educational Records",
          price: "$2,500.00",
          details: `Parents are not proficient in the IEP Process and can continue on
          their own to be effective advocates for their child. Certificate of
          Completion as having acquired the skill set level of an effective
          advocator for their child. Parents have the opportunity to pay a
          membership fee for services for P.O.S.S.E. to assist with future IEP
          for their child until 12th grade and assistance with College
          Preparatory Services with P.O.S.S.E.'s affiliate. Services of all
          above and Extensive Detailed Timeline regarding educational time
          records of child through current grade level; Continued Training of
          Parent; classroom observations if applicable; Visit of campus site
          regarding appropriate placement per the goals and objectives of the
          IEP; Attendance at all IEP meetings. Notes from IEP Meetings for
          Parents to add as a Addendum to meeting notes; Review draft IEP with
          Parents and continue until final IEP is in place for the child.
          Assistance with Transitional services for child if appropriate;
          Assistance with Extended School Year. Assistance with preparing
          Transition Assessments for future preparation for getting a job or
          college, live independently and participate in the community.
          Assistance with Transition Assessments is a step to helping your child
          set goals in the future.`,
          anticipatedDetails: `Parents are now trained to be an effective advocate for their child
          until graduation and can determine if services provided by the school
          are meeting the child’s needs and is the school providing a FAPE [Free
          Appropriate Public Education].`,
        },
      ],
      shoppingCart: [],
    };
  },
  methods: {
    addToList: (item: string) => {
      if (!item) return;
      // Split the string at the comma
      // Create an object
      // Push that object into the array list
      // Prams should be title & price
    },
    removeFromList: (item: string) => {
      // Split the string at the comma
      // Use the title to search if that's item is in the array
      // remove that item from the purchase list
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
</style>
