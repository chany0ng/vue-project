<template>
  <ProductList :products="products" />
</template>

<script>
// import GreetingUser from "./components/GreetingUser.vue";
import ProductList from "./components/ProductList.vue";
export default {
  name: "App",
  data() {
    return {
      products: [
        { id: 1, name: "TV", price: 500000, company: "LG" },
        { id: 2, name: "전자레인지", price: 100000, company: "삼성" },
        { id: 3, name: "오븐", price: 200000, company: "한화" },
        { id: 4, name: "냉장고", price: 1000000, company: "대우" },
        { id: 5, name: "에어컨", price: 2000000, company: "해태" },
      ],
    };
  },
  computed: {},
  directives: {},
  methods: {},
  watch: {},
  components: { ProductList },
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
