<template>
  <div class="card">
    <div v-if="isOperationTypeInput(operationType)" class="top-right-green">
      <div class="circle">
        <img src="../../public/img/arrow-down.png" alt="">
      </div>
    </div>
    <div v-else class="top-right-red">
      <div class="circle">
        <img src="../../public/img/arrow-up.png" alt="">
      </div>
    </div>
    <div class="center">
      <div class="number">{{amount}}</div>
    </div>
    <div class="bottom-left">
      <p>R$</p>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    amount: {
        type: Number,
        default: 0
    },
    operationType: {
        type: String
    }
  },
  methods: {
    isOperationTypeInput(value) {
        return value == "input"
    }
  }
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
  background-color: #EFF4FF; 
  border-radius: 0.7rem; 
  padding: 0.625rem; 
}

.top-right-green {
  position: absolute;
  top: 0.2rem;
  right: 0.3125rem; 
  background-color: #E6FFBE;
  border-radius: 0.7rem;
  width: 1.25rem; 
  height: 0.9375rem; 
  display: flex;
  justify-content: center;
  align-items: center;
}

.top-right-red {
  position: absolute;
  top: 0.2rem; 
  right: 0.3125rem;
  background-color: #FFE4E4;
  border-radius: 0.7rem; 
  width: 1.25rem; 
  height: 0.9375rem;
  display: flex;
  justify-content: center;
  align-items: center;
}

.center {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 0.5rem; 
}

.circle img{
    width: .5rem;
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