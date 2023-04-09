<template>
  <h2>Hello {{ username }}!</h2>
  <h3>오늘이 {{ numberOfVisits }} 번째 방문입니다.</h3>
  <h3>사이트 이름은 {{ siteInfo.name }} 입니다.</h3>
</template>
<script>
export default {
  name: "GreetingUser",
  props: {
    username: String,
    numberOfVisits: {
      type: Number,
      default: 0,
    },
    siteInfo: {
      type: Object,
      default: () => {
        return {};
      },
    },
  },
};
</script>
<style></style>
