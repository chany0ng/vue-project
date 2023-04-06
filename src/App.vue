<template>
  <!-- <h1>hello my name is {{ user.name }}</h1>
  <input type="text" v-model="user.name" /> -->
  <h2 v-if="showName">My name is {{ user.name }}</h2>
  <h2 v-else>이름을 보여줄 수 없습니다.</h2>
  <h2 v-if="user.age > 20">당신은 성인입니다.</h2>
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
