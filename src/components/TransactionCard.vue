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
  max-width: 5rem;
  width: 5rem;
  height: 5.6rem;
  background-color: #eff4ff;
  border-radius: 1.6rem;
  padding: 1.5rem;
}

.center {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 1.2rem;
}

.number {
  font-size: 2.4rem;
  margin-top: 5rem;
  color: #525151;
}

.bottom-left {
  position: absolute;
  bottom: 0;
  left: 1.2rem;
  width: 9rem;
  height: 2.2rem;
  display: flex;
  justify-content: left;
  align-items: center;
  color: #525151;
}

.bottom-left p {
  font-size: 1.2rem;
  margin: 0;
}
</style>