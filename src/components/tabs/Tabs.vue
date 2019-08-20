<template>
  <div class="tabs">
    <slot name="tab-heads"></slot>
    <div class="tab-panel">
      <slot :name="tabPanelSlotName"></slot>
    </div>
  </div>
</template>

<script>
import { EventBus } from "./eventBus.js";
export default {
  name: "Tabs",
  props: {
    initialTab: {
      type: String,
      required: true
    }
  },
  data() {
    return {
      activeTab: this.initialTab
    };
  },
  mounted() {
    EventBus.$on("tab-clicked", this.handleTabClick);
  },
  beforeDestroy() {
    EventBus.$off("tab-clicked");
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
};
</script>

<style scoped>
.tabs {
  margin: 30px auto;
  width: 90%;
  height: 70vh;
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
    width: 70%;
  }
}

@media (min-width: 991px) {
  .tabs {
    width: 50%;
  }
}
</style>