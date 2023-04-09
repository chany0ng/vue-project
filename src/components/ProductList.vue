<template>
  <ul>
    <ProductItem
      v-for="product of products"
      :key="product.id"
      :product="product"
    />
  </ul>
</template>
<script>
import ProductItem from "./ProductItem.vue";
export default {
  name: "product-list",
  components: {
    ProductItem,
  },
  props: {
    products: {
      type: Array,
      default: () => {
        return [];
      },
    },
  },
};
</script>
<style></style>
