<template lang="">
  <h2>component 3</h2>
  <h3>passed Data from App -> {{ name }}</h3>
</template>
<script>
export default {
  name: "complevel-3",
  data() {
    return {};
  },
  inject: ["name"],
};
</script>
<style lang=""></style>
