<template>
  <h2 v-if="showName">My name is {{ user.name }}</h2>
  <h2 v-else>이름을 보여줄 수 없습니다.</h2>
  <h2 v-if="user.age > 20">당신은 성인입니다.</h2>
</template>

<script>
export default {
  name: "App",
  data() {
<<<<<<< HEAD
    return {};
=======
>>>>>>> f1a8820 (조건부 리스트 렌더링)
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
</style>
