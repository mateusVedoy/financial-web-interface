<template>
  <div class="container">
    <div class="left-section">
      <LastTransactionsView class="float-right"/>
    </div>
    <div class="right-section">
      <BalanceCardView class="inner-card" />
      <TransactionHistoryView class="inner-card" />
    </div>
  </div>
</template>
<script>
import BalanceCardView from "@/components/BalanceCard.vue";
import LastTransactionsView from "./LastTransactions.vue";
import TransactionHistoryView from "./TransactionHistory.vue";

export default {
  name: "FinancialBoardView",
  components: {
    LastTransactionsView,
    BalanceCardView,
    TransactionHistoryView,
  },
};
</script>
<style scoped>
.inner-card {
  float: left;
  margin: 2rem 0 0 0;
}
.float-right {
  float: right;
}
.container {
  display: flex;
  justify-content: space-around;
  background-color: #f6f6f6;
  padding: 2rem;
}
.container > div {
  align-items: center;
  justify-content: center;
}
.left-section {
  width: 35%;
  float: left;
}
.right-section {
  justify-content: space-around;
  width: 60%;
  min-height: 100%;
  float: right;
}
</style>