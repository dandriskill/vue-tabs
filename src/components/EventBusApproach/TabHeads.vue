<template>
  <ul class="tab-heads">
    <slot></slot>
  </ul>
</template>

<script>
export default {
  name: "TabHeads"
};
</script>

<style scoped>
.tab-heads {
  margin: 0;
  padding: 10px 0 0 0;
  list-style: none;
  display: flex;
  justify-content: center;
  background: #f1f2f2;
}
</style>