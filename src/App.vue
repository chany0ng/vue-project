<template>
  <ul>
    <!-- template태그는 불필요한 DOM을 생성하지 않는다. -->
    <template v-for="(city, index) of cities" v-bind:key="index">
      <li v-if="city.province === '경상도'">
        {{ city.name }}
      </li>
    </template>
  </ul>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      cities: [
        { name: "서울", province: "경기도" },
        { name: "대전", province: "충청도" },
        { name: "인천", province: "경기도" },
        { name: "대구", province: "경상도" },
        { name: "부산", province: "경상도" },
        { name: "광주", province: "전라도" },
        { name: "제주", province: "제주도" },
      ],
    };
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
