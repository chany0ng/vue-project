<template>
  <div>{{ user }}</div>
  <hr />
  <form action="">
    <!-- 이름 입력하는 곳 -->
    <div>
      <label for="name">이름</label>
      <input type="text" id="name" v-model="user.name" @input="setValue" />
    </div>
    <!-- 나이 입력하는 곳 -->
    <div>
      <label for="age">나이</label>
      <input type="text" id="age" v-model="user.age" />
    </div>
    <!-- 사는 곳을 select option으로 체크 -->
    <div>
      <label for="city">사는 곳</label>
      <select name="" id="city" v-model="user.city">
        <option value="seoul">서울</option>
        <option value="daejeon">대전</option>
        <option value="daegu">대구</option>
        <option value="busan">부산</option>
        <option value="jeju">제주</option>
      </select>
    </div>
    <!-- 좋아하는 음식을 select option으로 선택 -->
    <div>
      <label for="food">음식</label>
      <select multiple id="food" v-model="user.food">
        <option value="JJ">짜장면</option>
        <option value="JB">짬뽕</option>
        <option value="TSY">탕수육</option>
      </select>
    </div>
    <!-- 내 직업을 체크박스로 하나만 선택 -->
    <div>
      <label for="job">직업</label>
      프로그래머<input type="checkbox" value="programmer" v-model="user.job" />
      가수<input type="checkbox" value="singer" v-model="user.job" /> 교사<input
        type="checkbox"
        value="teacher"
        v-model="user.job"
      />
    </div>
  </form>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      user: {
        name: "",
        age: 0,
        city: "",
        food: [],
        job: [],
      },
      foodOptions: [{ 짜장면: "JJ" }, { 짬뽕: "JB" }, { 탕수육: "TSY" }],
    };
  },
  methods: {
    setValue(e) {
      this.user.name = e.target.value;
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
