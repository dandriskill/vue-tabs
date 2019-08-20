<template>
  <div id="app">
    <Tabs initialTab="description">
      <TabHeads slot="tab-heads">
        <TabHead name="description">
          <img
            src="https://image.flaticon.com/icons/svg/1500/1500427.svg"
            alt="description-icon"
            class="tab-head-image"
          />
          <p class="tab-head-title">
            Description
          </p>
        </TabHead>
        <TabHead name="features">
          <img
            src="https://image.flaticon.com/icons/svg/756/756611.svg"
            alt="features-icon"
            class="tab-head-image"
          />
          <p class="tab-head-title">
            Features
          </p>
        </TabHead>
        <TabHead name="reviews">
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
    <div class="attributions">
      <div>
        Icons made by 
        <a href="https://www.flaticon.com/authors/srip" title="srip">srip</a>, 
        <a href="https://www.flaticon.com/authors/smartline" title="Smartline">Smartline</a>, 
        and <a href="https://www.flaticon.com/authors/freepik" title="Freepik">Freepik</a> 
        from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a> 
        is licensed by 
        <a href="http://creativecommons.org/licenses/by/3.0/" title="Creative Commons BY 3.0" target="_blank">
          CC 3.0 BY
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import Tabs from "./components/tabs/Tabs.vue";
import TabHeads from "./components/tabs/TabHeads.vue";
import TabHead from "./components/tabs/TabHead.vue";
import TabPanel from "./components/tabs/TabPanel.vue";

export default {
  name: "app",
  components: {
    Tabs,
    TabHeads,
    TabHead,
    TabPanel
  }
}
</script>

<style>
body {
  margin: 0;
}

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.attributions {
  width: 100%;
  display: flex;
  justify-content: center;
  position: absolute;
  bottom: 5px;
}
</style>
