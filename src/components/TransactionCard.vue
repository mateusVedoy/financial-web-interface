<template>
  <div class="card">
    <TransactionStatusComponent :operator="operationType" />
    <div class="center">
      <div class="number">{{ amount }}</div>
    </div>
    <div class="bottom-left">
      <p>R$</p>
    </div>
  </div>
</template>
<script>
import TransactionStatusComponent from "./TransactionStatus.vue";
export default {
  components: {
    TransactionStatusComponent,
  },
  props: {
    amount: {
      type: Number,
      default: 0,
    },
    operationType: {
      type: String,
    },
  },
};
</script>
<style scoped>
html {
  font-size: 16px;
}

.card {
  position: relative;
  font-family: "Courier New", Courier, monospace;
  max-width: 3.125rem;
  width: 3.125rem;
  height: 2.34375rem;
  background-color: #eff4ff;
  border-radius: 0.7rem;
  padding: 0.625rem;
}

.center {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 0.5rem;
}

.number {
  font-size: 1rem;
  margin-top: 2rem;
}

.bottom-left {
  position: absolute;
  bottom: 0;
  left: 0.5rem;
  width: 3.125rem;
  height: 0.9375rem;
  display: flex;
  justify-content: left;
  align-items: center;
}

.bottom-left p {
  font-size: 0.5rem;
  margin: 0;
}
</style>