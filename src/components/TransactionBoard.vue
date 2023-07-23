<template>
  <div class="board">
    <div class="title">
      <h1>Last Transactions</h1>
    </div>
    <div class="content">
      <TransactionCardComponent :amount="4750.0" :operationType="'input'" />
      <TransactionCardComponent :amount="27" :operationType="'output'" />
      <TransactionCardComponent :amount="4750.0" :operationType="'input'" />
      <TransactionCardComponent :amount="27" :operationType="'output'" />
      <TransactionCardComponent :amount="4750.0" :operationType="'input'" />
      <TransactionCardComponent :amount="27" :operationType="'output'" />
      <TransactionCardComponent :amount="4750.0" :operationType="'input'" />
      <TransactionCardComponent :amount="27" :operationType="'output'" />
      <TransactionCardComponent :amount="4750.0" :operationType="'input'" />
      <TransactionCardComponent :amount="27" :operationType="'output'" />
    </div>
  </div>
</template>
<script>
import TransactionCardComponent from "./TransactionCard.vue";
export default {
  name: "TransactionBoardComponent",
  components: {
    TransactionCardComponent,
  },
};
</script>
<style scoped>
.title {
  margin-bottom: 1.5em;
}
.title h1 {
  font-size: 1.2em;
  font-family: "Courier New", Courier, monospace;
  color: #898D93;
}
.board {
  box-shadow: .05rem .05rem rgba(82, 81, 81,.1);
  padding: 1.2em;
  border-radius: 1.2rem;
  width: 21em;
}
.content {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 1.5rem;
}
</style>