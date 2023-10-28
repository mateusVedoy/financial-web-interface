<template>
  <div class="container">
    <div class="left-section">
      <LastTransactionsView class="float-right" />
    </div>
    <div class="right-section">
      <BalanceToPeriodView class="inner-card" />
      <TransactionHistoryView class="inner-card" />
      <CalendarView class="top-right-pined"/>
    </div>
  </div>
</template>
<script>
import BalanceToPeriodView from "./BalanceToPeriod.vue";
import LastTransactionsView from "./LastTransactions.vue";
import TransactionHistoryView from "./TransactionHistory.vue";
import CalendarView from "./Calendar.vue"

export default {
  name: "FinancialBoardView",
  components: {
    LastTransactionsView,
    BalanceToPeriodView,
    TransactionHistoryView,
    CalendarView
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

.top-right-pined {
  position: absolute;
  top: 0;
  right: 0;
}

.container {
  display: flex;
  justify-content: space-around;
  background-color: #f6f6f6;
  padding: 1rem;
}

.container>div {
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
}</style>