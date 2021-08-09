<template>
  <div>
    <Nav />
    <div class="services-wrapper">
      <div class="services-intro">
        <h3 class="services-title">
          SERVICES WE PROVIDE
        </h3>
        <p>
          <b>PARENTS OF STUDENTS IN SPECIAL EDUCATION (P.O.S.S.E, Inc.)</b>
          provides individual advocacy and representation to children with
          learning disabilities. <b>P.O.S.S.E.</b> provides advocacy assistance
          to parents and families of children who may be suspected of having a
          learning disability and are in need of special education services or a
          504 Accommodation Plan. P.O.S.S.E. also offers independent consulting
          with legal professionals, doctors and agencies, as needed for the
          child’s individual needs and provides other services to parents and
          families of children with special needs. Some of the services offered
          by P.O.S.S.E are:
        </p>
      </div>
      <div class="service-list">
        <div v-for="i in list" :key="i.index">
          {{ i.service }}
        </div>
      </div>
      <div class="services-intro">
        <h3 class="services-title">
          SELECT EDUCATIONAL <br />SERVICES ORGANIZATIONS
        </h3>
        <p>
          Following is a list of organizations that collaborate with Parents of
          Students in Special Education. For more information about the
          educational services they provide, please contact them directly.
        </p>
      </div>
      <div class="services-list">
        <div
          class="services-profile"
          v-for="service in serviceList"
          :key="service.index"
        >
          <h3>{{ service.name ? service.name : null }}</h3>

          <div class="service-position">
            {{ service.jobType ? service.jobType : null }}
          </div>
          <div class="service-address">
            {{ service.address ? service.address : null }}
          </div>
          <div class="service-website">
            {{ service.website ? service.website : null }}
          </div>
          <div class="service-phone">
            <a
              role="button"
              :href="service.phone ? `tel:${service.phone}` : null"
              >Call</a
            >
          </div>
          <div class="service-email">
            <a :href="service.contact ? `mailto:${service.contact}` : null"
              >email</a
            >
          </div>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import { Slider, SliderItem } from "vue-easy-slider";

export default Vue.extend({
  data() {
    const list: any[] = [
      {
        service:
          "Individual Child Timeline Preparation of Entire School Records/History for Parent and Advocate in Preparation of IEP Meetings"
      },
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
    const serviceList: any[] = [
      {
        name: "Dr. Lynne Thrope, Ph.D.",
        jobType: "Reading Therapist",
        roomLocation: "The Reading Room",
        address: `2341-A Needham Road
          El Cajon, CA 92020`,
        website: "www.thereadingroom.net",
        phone: "6194643647",
        contact: null
      },
      {
        name: "Susan Monken",
        jobType: "Educational Consultant",
        roomLocation: "The Reading Room",
        address: `705 Fresca Street
Solana Beach, CA 92075`,
        website: "www.susanmonken.com",
        phone: "8583440401",
        contact: "smonken@gmail.com"
      },
      {
        name: "Dana Tappen",
        jobType: "Speech & Language Therapist",
        roomLocation: "Total Education Services",
        address: `5151 Murphy Canyon Road, Suite 150
San Diego, California 92123`,
        website: "www.thereadingroom.net",
        phone: "6192754522",
        contact: "dtappen@tesidea.com"
      },
      {
        name: "John W. Dupler, PhD, BCIA",
        jobType: "Neurofeedback, Neuro–Imaging Assessment",
        roomLocation: null,
        address: `16935 W. Bernardo Drive, Suite 238
San Diego, CA 92127`,
        website: null,
        phone: null,
        contact: "neuro@cox.net"
      }
    ];
    return {
      serviceList,
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
  &-email {
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
