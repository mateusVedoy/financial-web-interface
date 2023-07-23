<template>
  <div v-if="itsShowTotalInputAmount(option)" class="icon bg-color-green">
    <div class="arrow">
      <img src="../../public/img/arrow-down.png" alt="" />
    </div>
    <div class="balance">
      <p>{{ amount }}R$</p>
    </div>
  </div>
  <div v-else class="icon bg-color-red">
    <div class="arrow">
      <img src="../../public/img/arrow-up.png" alt="" />
    </div>
    <div class="balance">
      <p>{{ amount }}R$</p>
    </div>
  </div>
</template>
<script>
export default {
  name: "BalanceStatusComponent",
  props: {
    amount: {
      type: String,
    },
    option: {
      type: String,
    },
  },
  methods: {
    itsShowTotalInputAmount(option) {
      return option == "inputs";
    },
  },
};
</script>
<style scoped>
.icon {
  width: 8rem;
  height: 3rem;
  display: flex;
  gap: 0.4rem;
  border-radius: 1.6rem;
}
.arrow {
  width: 40%;
  height: 100%;
  position: relative;
  top: 01rem;
  left: 1rem;
}
.bg-color-green {
  background-color: #e6ffbe;
  color: #349014;
}
.bg-color-red {
  background-color: #ffe4e4;
  color: #902A14;
}
.arrow img {
  width: 1.2rem;
}
.balance {
  width: 60%;
  height: 100%;
  font-family: "Courier New", Courier, monospace;
}
</style>