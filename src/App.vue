<template>
  <h1>main에서도 무엇인가 바뀐게 있어야지 안그래?</h1>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      showName: false,
      user: {
        name: "chany0ng",
        age: 100,
        job: "prosexer",
      },
    };
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

.line-through {
  text-decoration: line-through;
}
.highlight {
  background-color: pink;
  opacity: 0.8;
  font-weight: bold;
}
</style>

const arr = [ {name: "a", age: 1}, {name: "b", age: 2}, {name: "c", age: 1},
{name: "a", age: 2}, {name: "b", age: 2}, {name: "c", age: 1}, ]
