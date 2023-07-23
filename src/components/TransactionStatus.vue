<template>
  <div v-if="isOperationTypeAnInput(operator)" class="top-right-green">
    <div class="circle">
      <img src="../../public/img/arrow-down.png" alt="" />
    </div>
  </div>
  <div v-else class="top-right-red">
    <div class="circle">
      <img src="../../public/img/arrow-up.png" alt="" />
    </div>
  </div>
</template>
<script>
export default {
  name: "TransactionStatusComponent",
  props: {
    operator: {
      type: String,
    },
  },
  methods: {
    isOperationTypeAnInput(value) {
      return value == "input";
    },
  },
};
</script>
<style scoped>
.top-right-green {
  position: absolute;
  top: 0.4rem;
  right: 0.5rem;
  background-color: #e6ffbe;
  border-radius: 1.6rem;
  width: 3rem;
  height: 2.2rem;
  display: flex;
  justify-content: center;
  align-items: center;
}

.top-right-red {
  position: absolute;
  top: 0.4rem;
  right: 0.5rem;
  background-color: #ffe4e4;
  border-radius: 1.6rem;
  width: 3rem;
  height: 2.2rem;
  display: flex;
  justify-content: center;
  align-items: center;
}
.circle img {
  width: 1.2rem;
}
</style>