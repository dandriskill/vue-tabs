<template>
  <li
    class="tab-head"
    :class="isActiveStyles"
    @click="handleTabClick(tab)"
  >
    <slot></slot>
  </li>
</template>

<script>
export default {
  name: "TabHead",
  props: {
    tab: {
      type: String,
      required: true
    },
    activeTab: {
      type: String,
      required: true
    },
    handleTabClick: {
      type: Function,
      required: true
    }
  },
  computed: {
    isActiveStyles: function() {
      const isActive = this.tab === this.activeTab;
      return isActive ? "tab-head--active" : "";
    }
  }
};
</script>

<style scoped>
.tab-head {
  display: block;
  position: relative;
  top: 1px;
  opacity: 0.5;
  color: #484848;
  background: Transparent;
  border: 1px solid Transparent;
  cursor: pointer;
  padding: 0px 5px;
  width: 100%;
  max-width: 115px;
}
.tab-head--active {
  background: #f7f7f7;
  border: 1px solid #cecece;
  border-bottom-color: #f7f7f7;
  border-radius: 5px 5px 0px 0px;
  opacity: 1;
}
.tab-head-image {
  margin: 10px 0 0 0;
  width: 20px;
  height: 20px;
}
.tab-head-title {
    margin: 0;
}

@media (min-width: 448px) {
  .tab-head {
    display: flex;
    justify-content: center;
    align-content: center;
    flex-wrap: nowrap;
  }
  .tab-head-image {
    margin: 13px 10px 0 0;
    width: 15px;
    height: 15px;
  }
  .tab-head-title {
    margin: 10px 0;
  }
}
</style>