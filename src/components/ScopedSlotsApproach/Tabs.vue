<template>
  <div class="tabs">
    <slot
      name="tab-heads"
      :activeTab="activeTab"
      :handleTabClick="handleTabClick"
    ></slot>
    <div class="tab-panel">
      <slot :name="tabPanelSlotName"></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "Tabs",
  props: {
    defaultTab: {
      type: String,
      required: true
    }
  },
  data() {
    return {
      activeTab: this.defaultTab
    }
  },
  methods: {
    handleTabClick: function(tab) {
      this.activeTab = tab;
    }
  },
  computed: {
    tabPanelSlotName: function() {
      return `tab-panel-${this.activeTab}`;
    }
  }
}
</script>

<style scoped>
.tabs {
  margin: 10px auto;
  width: 90%;
  height: 40vh;
  background: #f7f7f7;
  border: 1px solid #cecece;
  border-radius: 3px;
}
.tab-panel {
  text-align: left;
  padding: 10px 10%;
  border-top: 1px solid #cecece;
}

@media (min-width: 448px) {
  .tabs {
    width: 400px;
    margin: 10px;
  }
}
</style>