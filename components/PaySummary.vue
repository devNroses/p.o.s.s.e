<template>
  <div class="review-container">
    <div class="review-header">
      <h4>IN YOUR PACK</h4>
    </div>
    <div class="item-wrapper">
      <div class="item-container">
        <div class="item-icon">Icon</div>
        <div class="item-title">
          <p>Level I: Consultation Phase</p>
        </div>
        <div class="item-price">$75.00</div>
      </div>
      <div class="item-container">
        <div class="item-icon">Icon</div>
        <div class="item-title">
          <p>Level II: Critical Assessment Phase</p>
        </div>
        <div class="item-price">$375.00</div>
      </div>
      <div class="item-container">
        <div class="item-icon">Icon</div>
        <div class="item-title">
          <p>Level III: Parent Notebook and Parent Training</p>
        </div>
        <div class="item-price">$1,075.00</div>
      </div>
      <div class="item-container">
        <div class="item-icon">Icon</div>
        <div class="item-title">
          <p>Level IV: Timeline Educational Records</p>
        </div>
        <div class="item-price">$2,500.00</div>
      </div>
    </div>
    <div class="total-container">
      <button>PayPal Button</button>
      <p>Total: $375.00</p>
    </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  data() {
    return {};
  },
  methods: {},
});
</script>

<style lang="scss" scoped>
.review {
  &-container {
    border: 1px solid #ccc;
     border-radius: 8px;
    background: 	#f7f7f7;
    display: flex;
    flex-direction: column;
    position: fixed;
    bottom: 45px;
    right: 45px;
    width: 400px;
    height: auto;
    -webkit-box-shadow: 0px 4px 10px -3px rgba(112,112,112,0.84); 
box-shadow: 0px 4px 10px -3px rgba(112,112,112,0.84);
  }

  &-header {
    background-color: #669139;
    color: white;
    padding: 2px 16px;

    h4 {
      font-weight: bold;
    }
  }
}
.item {
  &-container {
    display: flex;
    height: auto;
    padding-top: 5px;
    padding-bottom: 5px;
      border-bottom: 1px solid #ccc;
      &:last-child{
        border: none;
      }
    div {
      display: flex;
      align-items: center;
    }
  }
  &-icon{
    width: 45px;
    padding-left: 16px;
  }

  &-title{
    flex-wrap: wrap;
    width: 220px;
    padding-left: 5px;
    font-weight: 600;;
  }

  &-price{
    width: 80px;
    justify-content: flex-end;
    font-weight: 600;
   padding-left: 16px;
  }


}

.total{
  &-container{
    background-color: white;
    border-top: 1px solid #ccc;
    display: flex;
    justify-content: space-between;
    padding: 24px 16px;

    p{
      font-size: 18px;
      font-weight: bold;;
    }
  }
}
</style>
