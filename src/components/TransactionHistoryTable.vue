<template>
  <div>
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
    </table>
  </div>
  <div class="tbody-container">
    <table>
      <tbody>
        <tr v-for="transaction in transactionHistoryList" :key="transaction.id">
          <td style="width: 5rem">{{ transaction.id }}</td>
          <td>{{ transaction.type }}</td>
          <td v-if="isAmountInput(transaction.type)" id="amount-green">
            +{{ transaction.amount }}
          </td>
          <td v-else id="amount-red">-{{ transaction.amount }}</td>
          <td>{{ transaction.date }}</td>
          <td>{{ transaction.hour }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>
<script>
export default {
  name: "TransactionHistoryTableComponent",
  props: {
    transactionHistoryList: {
      type: Object,
    },
  },
  methods: {
    isAmountInput(value) {
      return value === "input";
    },
  },
};
</script>
<style scoped>
table {
  border-collapse: collapse;
  margin: 0.8rem 0;
  font-family: "Courier New", Courier, monospace;
  font-size: 1rem;
  min-width: 100%;
  color: #525151;
}
.tbody-container {
  max-height: 20rem;
  overflow-x: scroll;
}
.tbody-container tr {
  text-align: center;
}
th, td {
  padding: .8rem;
  width: 5rem;
}
table tbody tr:hover {
  background-color: #fafafa;
}
#amount-green {
  color: #329b01;
}
#amount-red {
  color: #b64040;
}
</style>