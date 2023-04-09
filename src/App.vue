<template>
  <h2>Hello components!</h2>
  <button @click="activeTab = 'Menu1'">Menu1</button>
  <button @click="activeTab = 'Menu2'">Menu2</button>
  <button @click="activeTab = 'Menu3'">Menu3</button>
  <keep-alive>
    <component :is="activeTab"></component>
  </keep-alive>
</template>

<script>
import Menu1 from "./components/tabitems/Menu1.vue";
import Menu2 from "./components/tabitems/Menu2.vue";
import Menu3 from "./components/tabitems/Menu3.vue";
export default {
  name: "App",
  data() {
    return {
      username: "scalper",
      activeTab: "Menu1",
    };
  },
  provide() {
    return {
      name: this.username,
    };
  },
  computed: {},
  directives: {},
  methods: {},
  watch: {},
  components: { Menu1, Menu2, Menu3 },
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
