<template>
  <div>
    <Nav />
    <div class="services-wrapper">
      <div class="services-intro">
        <h2 class="pageTitle">
          P.O.S.S.E. Services and Level Up
        </h2>
      </div>
      <div class="levelUp-wrapper">
        <div class="levelUp-price">
          <h3>Level I:Consultation Phase</h3>
          <h3>$75.00</h3>
        </div>

        <p>
          Conference with Parent(s) to discuss the overall performance of the
          child and child’s educational background through their grade level so
          P.O.S.S.E. can understand the child and understand their Learning
          Challenges. Discuss how the child qualified i.e.”Eligibility” for
          services. Discuss Parent’s role at their child’s IEP meeting; Discuss
          what Parents should expect in an IEP Meeting; Who should attend their
          child’s IEP meeting with relation to their child’s teachers.
          Anticipated/Expected Outcome: Parents become familiar and can begin to
          understand the in depth process of their child’s educational needs and
          begin to understand the IEP Process as it pertains to their child.
        </p>
      </div>

      <div class="levelUp-wrapper">
        <div class="levelUp-price">
          <h3>Level II: Critical Assessment Phase</h3>
          <h3>$375.00</h3>
        </div>

        <p>
          Initial Assessment of what tests have been given and if the school has
          done a thorough evaluation in all areas of suspected disability for
          the child. Review records Parents have from the school. Prepare detail
          written correspondence to School Prinicipal/District to obtain ALL
          records, test, assessments and protocols through grade level from all
          schools of child’s attendance. Determine based on school records
          whether child is performing at grade level or below grade level.
          Review Present levels of Performance (PLOP). Determine any unique
          needs that the child may have that are not identified by the school or
          on the IEP; Determine what services the school has employed to address
          each need; what will the child be able to accomplish as a result of
          the services. Review all IEP Goals and Objectives on the current IEP
          and fomer IEPs; Advice of additional assessments for the child.
        </p>

        <h4>
          Anticipated/Expected Outcome:
        </h4>
        <p>
          Parents will be able to make an informed decision as to where the
          child is performing grade level and if the child has made measurable
          educational gains as provided under IDEA.
        </p>
      </div>

      <div class="levelUp-wrapper">
        <div class="levelUp-price">
          <h3>Level III - P.O.S.S.E. Parent Notebook</h3>
          <h3>$1,075.00</h3>
        </div>

        <p>
          Parent receives notebook with all of child’s records in Chronological
          order with worksheet and progress sheets for upcoming IEP meetings,
          beginning of P.O.S.S.E. Training until completion of IEP process;
          preparation of Parent Agenda for Meetings; Review and discuss all
          Evaluation assessments that were given to child; Review and make sure
          Parents have all reports three days before the IEP Meeting to discuss
          at meeting; Pre-IEP meeting with Parent to address concerns;
          attendance at two IEP Meetings (Via Zoom) or in person if applicable;
          Recording of IEP Notices given.
        </p>

        <h4>
          Anticipated/Expected Outcome:
        </h4>
        <p>
          Parents are prepared to begin advocating for their child and
          understand what has to be provided by the school under IDEA and what
          their child is entitled to under the law on their child’s Independent
          Educational Plan.
        </p>
      </div>

      <div class="levelUp-wrapper">
        <div class="levelUp-price">
          <h3>Level IV</h3>
          <h3>$2,500.00</h3>
        </div>

        <p>
          Services of all above and Extensive Detailed Timeline regarding
          educational time records of child through current grade level;
          Continued Training of Parent; classroom observations if applicable;
          Visit of campus site regarding appropriate placement per the goals and
          objectives of the IEP; Attendance at all IEP meetings. Notes from IEP
          Meetings for Parents to add as a Addendum to meeting notes; Review
          draft IEP with Parents and continue until final IEP is in place for
          the child. Assistance with Transitional services for child if
          appropriate; Assistance with Extended School Year.
        </p>

        <h4>
          Anticipated/Expected Outcome:
        </h4>
        <p>
          Parents are now trained to be an effective advocate for their child
          until graduation and can determine if services provided by the school
          are meeting the child’s needs and is the school providing a FAPE [Free
          Appropriate Public Education].
        </p>
      </div>

      <div class="services-intro">
        <h2 class="pageTitle">
          Services
        </h2>
      </div>
      <div class="service-list">
        <div v-for="i in list" :key="i.index">
          {{ i.service }}
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
    const list: any[] = [
      {
        service:
          "Provide Parent Education together with Parent Working Notebook"
      },
      {
        service: "Attendance at IEP Team & 504 Plan Meetings"
      },
      {
        service: "Assistance with the Development of IEPs and 504 Plans"
      },
      {
        service:
          "Assistance with Letter Correspondence and Telephone Communication"
      },
      {
        service:
          "Assistance with Preparation of Evaluation Plans and or Assessment Plans"
      },
      {
        service: "School Site Visits for Appropriate Placements"
      },
      {
        service: "Classroom Observations"
      },
      {
        service:
          "Assistance with Resolving Disputes with School District, or other Agency Providing Services"
      },
      {
        service: "IEP Team Meeting Preparation with Parents"
      },
      {
        service: "Provide Relevant Resources and Referrals"
      }
    ];

    return {
      list
    };
  },
  methods: {}
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
      margin-top: 10px;
      margin-bottom: 5px;
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
    margin: 0 auto 40px;

    h4 {
      margin-bottom: -10px;
    }
  }

  &-price {
    display: flex;
    justify-content: space-between;
    border-bottom: 1px solid gray;
    margin-bottom: 5px;
  }
}
</style>
