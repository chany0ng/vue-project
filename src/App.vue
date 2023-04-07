<template>
  <div v-for="(animal, index) in animals" :key="index">
    <h2>Animal ==> {{ animal.name }}</h2>
    <h3>food</h3>
    <ul>
      <li v-for="(food, index) of animal.food" :key="index">
        {{ food }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      animals: [
        {
          name: "monkey",
          size: "medium",
          food: ["banana", "apple"],
        },
        {
          name: "tiger",
          size: "big",
          food: ["deer", "cow"],
        },
        {
          name: "rat",
          size: "small",
          food: ["cheese", "rice"],
        },
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
