<template>
  <BalanceCardComponent
    :inputAmount="inputs"
    :outputAmount="outputs"
    :balance="balance"
  />
</template>
<script>
import BalanceCardComponent from "@/components/BalanceCard.vue";
export default {
  name: "BalanceToPeriodView",
  components: {
    BalanceCardComponent,
  },
};
</script>