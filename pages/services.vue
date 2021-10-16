<template>
  <div>
    <Nav />
    <div class="services-wrapper">
      <div class="services-intro">
        <h3 class="services-title">
          P.O.S.S.E. Services
        </h3>
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
</style>
