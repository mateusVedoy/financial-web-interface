<template>
  <table>
    <thead>
      <tr>
        <th>ID</th>
        <th>Transfer Type</th>
        <th>Amount</th>
        <th>Date</th>
        <th>Hour</th>
      </tr>
    </thead>
    <tbody v-for="transaction in transactionHistoryList" :key="transaction.id">
      <tr>
        <td>{{transaction.id}}</td>
        <td>{{transaction.type}}</td>
        <td v-if="isAmountInput(transaction.type)" id="amount-green">+{{transaction.amount}}</td>
        <td v-else id="amount-red">-{{transaction.amount}}</td>
        <td>{{transaction.date}}</td>
        <td>{{transaction.hour}}</td>
      </tr>
    </tbody>
  </table>
</template>
<script>
export default {
  name: "TransactionHistoryTableComponent",
  props: {
    transactionHistoryList: {
      type: Object
    },
  },
  methods: {
    isAmountInput(value) {
        return value === "input";
    }
  }
};
</script>
<style scoped>
table {
  border-collapse: collapse;
  margin: 2rem 0;
  font-family: "Courier New", Courier, monospace;
  font-size: 1rem;
  min-width: 100%;
  color: #525151;
}
table thead tr {
  text-align: center;
}
table thead th {
  margin-left: 5rem;
}
table tbody tr {
  text-align: center;
}
th,
td {
  padding: 0.8rem 0.8rem;
}
table tbody tr:hover {
    background-color: #fafafa;
}
#amount-green {
    color: #329B01;
}
#amount-red {
    color: #B64040;
}
</style>