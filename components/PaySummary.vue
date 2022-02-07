<template>
  <div class="review-container">
    <div class="review-header">
      <h4>IN YOUR PACK</h4>
      <span>({{ purchaseList.length }})</span>
    </div>
    <div v-if="purchaseList.length" class="item-wrapper">
      <div class="item-container" v-for="(item, i) of purchaseList" :key="i">
        <div class="item-icon">Icon</div>
        <div class="item-title">
          <p>{{ item.name }}</p>
        </div>
        <div class="item-price">{{ `$${item.price}.00` }}</div>
      </div>
    </div>
    <div v-else class="empty-cart">
      <img src="~/../assets/imgs/shopping_add.svg" />
      <p>
        Add one or more of our amazing services,<br />so your cart is not so
        empty.
      </p>
    </div>
    <div v-if="purchaseList.length" class="total-container">
      <p>Total: {{ total }}</p>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  data() {
    return {
      total: 0,
    };
  },
  props: ["purchaseList"],
  methods: {
    calculate() {},
  },
});
</script>

<style lang="scss" scoped>
.review {
  &-container {
    border: 1px solid #ccc;
    border-radius: 8px;
    background: #f7f7f7;
    display: flex;
    flex-direction: column;
    position: fixed;
    bottom: 45px;
    right: 45px;
    width: 400px;
    height: auto;
    -webkit-box-shadow: 0px 4px 10px -3px rgba(112, 112, 112, 0.84);
    box-shadow: 0px 4px 10px -3px rgba(112, 112, 112, 0.84);
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
    &:last-child {
      border: none;
    }
    div {
      display: flex;
      align-items: center;
    }
  }
  &-icon {
    width: 45px;
    padding-left: 16px;
  }

  &-title {
    flex-wrap: wrap;
    width: 220px;
    padding-left: 5px;
    font-weight: 600;
  }

  &-price {
    width: 80px;
    justify-content: flex-end;
    font-weight: 600;
    padding-left: 16px;
  }
}

.total {
  &-container {
    background-color: white;
    border-top: 1px solid #ccc;
    display: flex;
    justify-content: space-between;
    padding: 24px 16px;

    p {
      font-size: 18px;
      font-weight: bold;
    }
  }
}

.empty-cart {
  min-height: 150px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  font-size: 18px;
  font-weight: 400;

  p {
    padding-bottom: 15px;
  }

  img {
    width: 120px;
    margin-bottom: -20px;
  }
}
</style>
