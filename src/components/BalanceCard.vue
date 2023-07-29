<template>
  <div class="card">
    <div class="top">
      <div>
        <h2>Balance To Period</h2>
      </div>
      <div class="status">
        <BalanceStatusComponent :option="'inputs'" :amount="inputAmount" />
        <BalanceStatusComponent :option="'outputs'" :amount="outputAmount" />
      </div>
    </div>
    <div class="amount">
      <p>{{ balance }}R$</p>
    </div>
    <div class="bottom">
      <div class="btn-deposit"><h3>Deposit</h3></div>
      <div class="btn-withdraw"><h3>Withdraw</h3></div>
    </div>
  </div>
</template>
<script>
import BalanceStatusComponent from "./BalanceStatus.vue";
export default {
  name: "BalanceCardComponent",
  components: {
    BalanceStatusComponent,
  },
  props: {
    inputAmount: {
      type: Number,
      default: 0,
    },
    outputAmount: {
      type: Number,
      default: 0,
    },
    balance: {
      type: Number,
      default: 0,
    },
  },
};
</script>
<style scoped>
.card {
  width: 56rem;
  height: 20rem;
  border-radius: 1.5rem;
  box-sizing: border-box;
  background-color: #ffff;
}
.top {
  width: 100%;
  height: 20%;
  padding-top: 0.2rem;
  display: flex;
}
.top > div {
  width: 50%;
}
.top h2 {
  font-family: "Courier New", Courier, monospace;
  color: #898d93;
  margin-left: 2rem;
}
.status {
  margin-left: 5rem;
  display: flex;
  align-items: center;
  gap: 2rem;
  justify-content: center;
}
.amount {
  height: 45%;
  display: flex;
  align-items: center;
  justify-content: center;
}
.amount p {
  font-family: "Courier New", Courier, monospace;
  color: #525151;
  font-size: 5rem;
}
.bottom {
  height: 30%;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 5rem;
}
.bottom > div {
  width: 15rem;
  height: 5rem;
  border-radius: 1.6rem;
  display: flex;
  align-items: center;
  justify-content: center;
}
.bottom > div > h3 {
  font-size: 2rem;
  font-family: "Courier New", Courier, monospace;
}
.btn-deposit {
  background-color: #8694c7;
  color: #dfdfdf;
}
.btn-withdraw {
  background-color: #e6e7ea;
  color: #8694c7;
}
.btn-deposit:hover {
  transition: 0.2s;
  background-color: #9dabdb;
  color: #f1f3f5;
}
.btn-withdraw:hover {
  transition: 0.2s;
  background-color: #e8eaee;
  color: #a2afdf;
}
</style>