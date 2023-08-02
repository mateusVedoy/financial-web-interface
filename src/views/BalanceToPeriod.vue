<template>
  <BalanceCardComponent
    :inputAmount="inputs"
    :outputAmount="outputs"
    :balance="amount"
  />
</template>
<script>
import BalanceCardComponent from "@/components/BalanceCard.vue";
export default {
  name: "BalanceToPeriodView",
  components: {
    BalanceCardComponent,
  },
  data() {
    return {
      inputs: null,
      outputs: null,
      amount: null,
    };
  },
  methods: {
    async getBalanceAnalytics() {
      this.inputs = 1;
      this.outputs = 2;
      this.amount = 3;
    },
  },
  async beforeMount() {
    await this.getBalanceAnalytics();
  },
};
</script>