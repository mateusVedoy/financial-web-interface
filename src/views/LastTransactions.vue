<template>
  <TransactionBoardComponent :transactions="last_transactions" />
</template>
<script>
import TransactionBoardComponent from "@/components/TransactionBoard.vue";

export default {
  name: "LastTransactionsView",
  components: {
    TransactionBoardComponent,
  },
  data() {
    return {
      last_transactions: null,
    };
  },
  methods: {
    //TODO: gerar endpoint de last transactions
    async getLastTransactions() {
      const request = await fetch(
        "http://127.0.0.1:8081/api/finances/operation/find/all"
      );
      const {data} = await request.json();
      this.last_transactions = data;
    },
  },
  async beforeMount() {
    await this.getLastTransactions();
  },
};
</script>