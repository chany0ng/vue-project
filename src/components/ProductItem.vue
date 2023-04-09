<template lang="">
  <li>
    <p class="title">{{ product.name }}</p>
    <p class="image">
      <img
        :src="`https://placeimg.com/200/100/${product.id}`"
        :alt="product.name"
      />
    </p>
    <p class="price">{{ product.price }}</p>
    <!-- <p class="company">{{ product.company }}</p> -->
  </li>
</template>

<script>
export default {
  name: "product-item",
  props: {
    product: {
      type: Object,
    },
  },
};
</script>

<style scoped>
.title {
  font-size: 24px;
  color: #2c82c9;
  font-weight: bold;
}
li {
  border: 2px solid salmon;
  margin-bottom: 10px;
}
</style>
