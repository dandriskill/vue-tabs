<template>
  <div id="app">
    <div class="different-way-to-build-modular-tabs">
      <span>
        <h1>HOC Approach</h1>
        <!-- <HigherOrderComponentApproach /> -->
      </span>
      <span>
        <h1>Scoped Slots Approach</h1>
        <ScopedSlotsApproach />
      </span>
      <span>
        <h1>Event Bus Approach</h1>
        <EventBusApproach />
      </span>
    </div>
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
// import HigherOrderComponentApproach from "./componets/HigherOrderComponentApproach";
import ScopedSlotsApproach from "./components/ScopedSlotsApproach";
import EventBusApproach from "./components/EventBusApproach";

export default {
  name: "app",
  components: {
    // HigherOrderComponentApproach,
    ScopedSlotsApproach,
    EventBusApproach
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
  color: #2c3e50;
}

.different-way-to-build-modular-tabs {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  text-align: center;
}

.attributions {
  width: 100%;
  display: flex;
  justify-content: center;
  margin-top: 100px;
}
</style>
