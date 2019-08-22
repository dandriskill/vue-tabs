<template>
  <span>
    <slot></slot>
  </span>
</template>

<script>
export default {
  name: "TabPanel"
};
</script>

<style scope>
.product-review {
  display: flex;
  justify-content: space-between;
  flex-wrap: nowrap;
  border-bottom: 1px solid #cecece;
}
</style>
