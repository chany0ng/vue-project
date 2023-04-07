<template>
  <h1>Hello {{ name }}!</h1>
  <button v-on:click="changeName">change name</button>
  <button v-on:mouseover="name = 'code sibal'" v-on:mouseleave="changeName">
    change name
  </button>
  <a
    v-on:click.prevent="movePage"
    href="http://www.naver.com"
    target="_blank"
    rel="noopener noreferrer"
    >네이버로 가자</a
  >
  <h2>{{ number }}</h2>
  <button v-on:click="number += 1">숫자증가</button>
  <button v-on:click="number -= 1">숫자감소</button>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      name: "chanyong",
      number: 0,
    };
  },
  methods: {
    changeName() {
      this.name = "Code chanyong";
    },
    movePage() {
      const check = confirm("페이지를 이동할거?");
      if (check) console.log("tlqkf");
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
</style>
