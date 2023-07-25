<template>
  <div class="board">
    <div class="title">
      <h1>Last Transactions</h1>
    </div>
    <div class="content">
      <div v-for="transaction in transactions" :key="transaction.id">
        <TransactionCardComponent
          :amount="transaction.amount"
          :operationType="transaction.type"
        />
      </div>
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
  props: {
    transactions: {
      type: Object,
    },
  },
};
</script>
<style scoped>
.title {
  margin-bottom: 1.5em;
}
.title h1 {
  font-size: 1.5em;
  font-family: "Courier New", Courier, monospace;
  color: #898d93;
}
.board {
  padding: 1.2em 1.2rem 3rem 1.2rem;
  border-radius: 1.2rem;
  width: 30em;
  min-height: 50rem;
  background-color: #ffff;
}
.content {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 2rem;
}
</style>