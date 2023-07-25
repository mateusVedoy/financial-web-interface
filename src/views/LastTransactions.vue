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
  props: {
    lastTransactions: {
      type: Object,
    },
  },
  data() {
    return {
      last_transactions: null,
    };
  },
  methods: {
    //consulta fake simulando as chamadas finais e reais
    async getLastTransactions() {
      const request = await fetch(
        "https://webhook.site/cd3bad25-5920-4029-90e1-95c175da80e8"
      );
      const data = await request.json();
      console.log(data);
      this.last_transactions = data;
    },
  },
  async beforeMount() {
    await this.getLastTransactions();
  },
};
</script>