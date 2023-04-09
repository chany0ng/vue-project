<template>
  <h1>watchers</h1>
  <h2>Current money: {{ money }}</h2>
  <div>
    <button @click="money += 100">earn money</button>
    <button @click="money -= 100">spend money</button>
  </div>
  <h3>{{ receipt }}</h3>
  <button @click="receipt.food += 500">buy food</button>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      userName: "ChanYong",
      money: 0,
      receipt: {
        food: 3000,
        fee: 2000,
        fare: 10000,
      },
    };
  },
  computed: {},
  directives: {},
  methods: {},
  watch: {
    receipt: {
      handler(newValue) {
        console.log("영수증 값 변화: ", newValue);
      },
      deep: true,
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
a {
  font-size: 24px;
  display: block;
  text-decoration: none;
}
label {
  font-size: 22px;
  font-weight: bold;
  margin-right: 1rem;
}
div {
  margin-bottom: 1rem;
}
</style>
