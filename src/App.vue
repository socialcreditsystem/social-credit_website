<template>
  <div id="app">
    <Stage title="China's Social Credit System"/>
    <ChinaMap/>
  </div>
</template>

<script>
import Stage from "./components/Stage.vue";
import ChinaMap from "./components/ChinaMap.vue";

export default {
  name: "app",
  components: {
    Stage,
    ChinaMap
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
