<template>
  <div class="board">
    <div class="top">
      <div>
        <h2>Transaction History</h2>
      </div>
      <div>
        <div class="search-container">
          <input type="text" class="search-input" placeholder="Search" />
          <button class="search-button">
            <img src="../../public/img/search.png" alt="Search" />
          </button>
        </div>
      </div>
    </div>
    <div class="table">
      <TransactionHistoryTableComponent :transactionHistoryList="transactionHistoryValues"/>
    </div>
  </div>
</template>
<script>
import TransactionHistoryTableComponent from "./TransactionHistoryTable.vue";

export default {
  name: "TransactionHistoryBoardComponent",
  components: {
    TransactionHistoryTableComponent,
  },
  props: {
    transactionHistoryValues: {
      type: Object
    },
  },
};
</script>
<style scoped>
.board {
  width: 56rem;
  height: 30rem;
  border-radius: 1.6rem;
  background-color: #ffff;
}
.top {
  width: 100%;
  height: 15%;
  display: flex;
}
.top > div:first-child {
  height: 100%;
  width: 50%;
  display: inline;
}
.top > div:first-child h2 {
  font-family: "Courier New", Courier, monospace;
  font-weight: 100;
  color: #898d93;
  font-size: 1.5rem;
  margin-left: 1.5rem;
  margin-top: 2rem;
}
.top > div:last-child {
  display: flex;
  align-items: center;
  justify-content: center;
}
.search-container {
  margin-top: 1rem;
  margin-left: 5rem;
  display: flex;
  align-items: center;
  border-radius: 1rem;
  padding: 0.5rem;
  background-color: #e6e7ea;
}

.search-input {
  border: none;
  outline: none;
  width: 80%;
  padding: 0.2rem 0.7rem;
  font-size: 1.2rem;
  font-family: "Courier New", Courier, monospace;
  color: #898d93;
  background-color: #e6e7ea;
}

.search-button {
  border: none;
  background-color: transparent;
  outline: none;
  cursor: pointer;
  padding: 0.2rem;
}

.search-button img {
  width: 1.2rem;
}
</style>