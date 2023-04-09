<template lang="">
  <div class="card">
    <slot></slot>
  </div>
</template>
<script>
export default {};
</script>
<style scoped>
.card {
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.3);
  padding: 1rem;
  margin-bottom: 1rem;
  width: 200px;
}
.card:hover {
  transform: scale(1.05);
  transition: 0.1s ease-in-out;
  background-color: antiquewhite;
}
</style>
