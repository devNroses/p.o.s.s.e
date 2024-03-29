<template>
  <div>
    <div v-show="!showFullCart" v-on:click="toggleCartView" class="cartIcon">
      <img class="cartIcon-img" src="~/../assets/imgs/shopping_add_white.svg" />
      <span>{{ purchaseList.length }}</span>
    </div>
    <div v-show="showFullCart" class="review-container">
      <div class="review-header">
        <button v-on:click="toggleCartView">X</button>
      </div>
      <div v-if="purchaseList.length" class="item-wrapper">
        <div
          v-on:click="removeItem(item)"
          class="item-container"
          v-for="(item, i) of purchaseList"
          :key="i"
        >
          <div class="item-icon">
            <img src="~/../assets/imgs/shoppingTag.svg" />
          </div>
          <div id="itemTitle" class="item-title">
            <p>{{ item.name }}</p>
          </div>
          <div id="itemPrice" class="item-price">${{ `${item.price}` }}.00</div>
        </div>
      </div>
      <div v-else class="empty-cart">
        <img src="~/../assets/imgs/shopping_add.svg" />
        <p>Your cart is empty.</p>
      </div>
      <div v-show="purchaseList.length" class="total-container">
        <p>
          <b>Total:</b> $<span id="total-price">{{
            cartTotal.toLocaleString("en-US")
          }}</span>
        </p>
        <div id="purchaseButtons"></div>
        <div>
          <paypal-buttons />
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import { loadScript } from "@paypal/paypal-js";
export default Vue.extend({
  props: ["purchaseList", "cartTotal", "removeItem"],
  data() {
    return {
      showFullCart: false,
    };
  },
  methods: {
    toggleCartView() {
      this.showFullCart = !this.showFullCart;
    },
  },
  mounted: async () => {
    let paypal;
    let paypalTotalPrice = document.getElementById("total-price");
    paypalTotalPrice.addEventListener("DOMCharacterDataModified", () => {});

    if (!paypal) {
      try {
        paypal = await loadScript({
          "client-id":
            "ASqBo7j8sH4-ycYu9vWafVIOiRrQ8Bs4wLZIwI6ueFiMQ4_3hrEh0gpeTQYvPc_WaqhW6Fdfp5-hRq96",
        });
      } catch (error) {
        console.error("failed to load the PayPal JS SDK script", error);
      }
    }

    if (paypal) {
      try {
        await paypal
          .Buttons({
            createOrder: function (data, actions) {
              let paypalTotalPrice = document.getElementById("total-price");
              let listItems: any[] = [];
              let paypalItemsByTitle = document.querySelectorAll("#itemTitle");
              let paypalItemsByPrice = document.querySelectorAll("#itemPrice");

              for (let i = 0; i < paypalItemsByTitle.length; i++) {
                let firstSplit = paypalItemsByTitle[i]?.innerHTML.split(">");
                let descriptionName = firstSplit[1].split("<");
                listItems.push({
                  name: descriptionName[0],
                  description: "P.O.S.S.E. service",
                  quantity: "1",
                });
              }

              if (listItems.length > 0) {
                for (let i = 0; i < listItems.length; i++) {
                  let firstSplit = paypalItemsByPrice[i]?.innerHTML.split("$");
                  let itemPrice = firstSplit[1].split(".00");
                  listItems[i].unit_amount = {
                    currency_code: "USD",
                    value: itemPrice[0],
                  };
                }
              }

              return actions.order.create({
                purchase_units: [
                  {
                    amount: {
                      currency_code: "USD",
                      value: paypalTotalPrice.innerText
                        .replace(/\s/g, "")
                        .replace(/,/g, "") as string,
                      breakdown: {
                        item_total: {
                          /* Required when including the `items` array */
                          currency_code: "USD",
                          value: paypalTotalPrice.innerText
                            .replace(/\s/g, "")
                            .replace(/,/g, "") as string,
                        },
                      },
                    },
                    items: listItems,
                  },
                ],
              });
            },
            onApprove: function (data, actions) {
              // This function captures the funds from the transaction.
              return actions.order.capture().then(function (details) {
                // This function shows a transaction success message to your buyer.
                alert(
                  `Hi ${details.payer.name.given_name}, your transaction has been completed.`
                );
                // window.location.reload();
              });
            },
          })
          .render("#purchaseButtons");
      } catch (error) {
        console.error("failed to render the PayPal Buttons", error);
      }
    }
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
    max-width: 400px;
    min-width: 200px;
    width: auto;
    height: auto;
    -webkit-box-shadow: 0px 4px 10px -3px rgba(112, 112, 112, 0.84);
    box-shadow: 0px 4px 10px -3px rgba(112, 112, 112, 0.84);

    @media only screen and (max-width: 390px) {
      right: 0;
      left: 0;
    }
  }

  &-header {
    background-color: #669139;
    color: white;
    padding: 12px 16px;
    display: flex;
    justify-content: flex-end;

    button {
      background: none;
      border: none;
      font-size: 20px;
      color: white;
      cursor: pointer;
    }

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
    &:hover {
      cursor: pointer;
    }
    &:last-child {
      border: none;
    }
    div {
      display: flex;
      align-items: center;
    }

    @media only screen and (max-width: 390px) {
      padding-right: 8px;
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
    justify-content: center;
    align-items: center;
    flex-direction: column;
    padding: 24px 16px;

    p {
      font-size: 20px;
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

.cartIcon {
  width: 90px;
  height: 90px;
  border-radius: 50%;
  background-color: #669139;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  position: fixed;
  bottom: 45px;
  right: 45px;
  cursor: pointer;

  img {
    stroke: white;
    width: 80px;
    margin-left: -20px;
    margin-top: -12px;
  }

  span {
    color: white;
    font-size: 20px;
    font-weight: bold;
    margin-left: -12px;
    margin-top: 28px;
  }
}
</style>
