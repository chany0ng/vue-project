<template>
  <h1>Hello guys!</h1>
  <button @click="displayDetail = !displayDetail">show detail</button>
  <DetailView v-if="displayDetail" @closeDetail="close" @sendData="showData" />
</template>

<script>
import DetailView from "./components/DetailView.vue";
export default {
  name: "App",
  data() {
    return {
      displayDetail: false,
    };
  },
  computed: {},
  directives: {},
  methods: {
    close() {
      this.displayDetail = false;
    },
    showData(data) {
      console.log(data);
    },
  },
  watch: {},
  components: { DetailView },
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
