<template>
  <div>
    <Tabs defaultTab="description">
      <TabHeads slot="tab-heads">
        <TabHead tab="description">
          <img
            src="https://image.flaticon.com/icons/svg/1500/1500427.svg"
            alt="description-icon"
            class="tab-head-image"
          />
          <p class="tab-head-title">
            Description
          </p>
        </TabHead>
        <TabHead tab="features">
          <img
            src="https://image.flaticon.com/icons/svg/756/756611.svg"
            alt="features-icon"
            class="tab-head-image"
          />
          <p class="tab-head-title">
            Features
          </p>
        </TabHead>
        <TabHead tab="reviews">
          <img
            src="https://image.flaticon.com/icons/svg/1243/1243552.svg"
            alt="reviews-icon"
            class="tab-head-image"
          />
          <p class="tab-head-title">
            Reviews
          </p>
        </TabHead>
      </TabHeads>
      <TabPanel slot="tab-panel-description">
        <h3>Description</h3>
        <p>
          This product is awesome. You should totally buy it.
          If you don't, can you at least tell your friends?
        </p> 
      </TabPanel>
      <TabPanel slot="tab-panel-features">
        <h3>Features</h3>
        <ul>
          <li>Lightweight.</li>
          <li>Adjustable straps.</li>
          <li>Waterproof.</li>
          <li>Breathable design.</li>
          <li>Comes in a variety of colors.</li>
          <li>Lifetime warranty.</li>
          <li>Money-back guarantee!</li>
        </ul> 
      </TabPanel>
      <TabPanel slot="tab-panel-reviews">
        <h3>Reviews</h3>
        <div class="product-review">
          <p>This is a product review.</p>
        </div>
        <div class="product-review">
          <p>This is another product review.</p>
        </div>
        <div class="product-review">
          <p>This is yet another product review.</p>
        </div> 
      </TabPanel>
    </Tabs>
  </div>
</template>

<script>
import Tabs from "./Tabs.vue";
import TabHeads from "./TabHeads.vue";
import TabHead from "./TabHead.vue";
import TabPanel from "./TabPanel.vue";

export default {
  name: "EventBusApproach",
  components: {
    Tabs,
    TabHeads,
    TabHead,
    TabPanel
  }
}
</script>
