<template>
  <div>
    <h2>Hello Slots!</h2>
    <CardView> Hello Slot!!! </CardView>
    <CardView>
      <img src="https://placeimg.com/100/50/any" alt="random" />
    </CardView>
    <CardView>
      <ul>
        <li>짬뽕</li>
        <li>짜장</li>
      </ul>
    </CardView>
  </div>
</template>

<script>
import CardView from "./components/slot/CardView.vue";
export default {
  name: "App",
  data() {
    return {};
  },
  provide() {
    return {};
  },
  computed: {},
  directives: {},
  methods: {},
  watch: {},
  components: { CardView },
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
