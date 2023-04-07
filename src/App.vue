<template>
  <h2>나이: {{ add(5) }}</h2>
  <h2>나이: {{ add(10) }}</h2>
  <h2>나이: {{ add(15) }}</h2>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      age: 10,
    };
  },
  methods: {
    add(num) {
      console.log(num);
      return this.age + num;
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
</style>
