<template>
  <TransactionCardComponent :amount="4450.00" :operationType="'input'" />
  <br>
  <TransactionCardComponent :amount="27" :operationType="'output'"/>
  <router-view />
</template>
<script>
import TransactionCardComponent from "./components/TransactionCard.vue";
export default {
  components: {
    TransactionCardComponent,
  },
};
</script>
<style>
</style>
