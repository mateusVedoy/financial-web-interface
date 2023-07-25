<template>
  <FinancialBoardView />
  <router-view />
</template>
<script>
import FinancialBoardView from './views/FinancialBoard.vue';
export default {
  components: {
    FinancialBoardView
  }
};
</script>
<style>
</style>
