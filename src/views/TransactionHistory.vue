<template>
  <TransactionHistoryBoardComponent :transactionHistoryValues="histories" />
</template>
<script>
import TransactionHistoryBoardComponent from "@/components/TransactionHistoryBoard.vue";
export default {
  name: "TransactionHistoryView",
  components: {
    TransactionHistoryBoardComponent,
  },
  data() {
    return{
        histories: null
    }
  },
  methods: {
    async getTransactionHistories() {
      const request = await fetch(
        "http://127.0.0.1:8081/api/finances/operation/find/all"
      );
      const {data} = await request.json();
      this.histories = data;
    },
  },
  async beforeMount() {
    await this.getTransactionHistories();
  },
};
</script>