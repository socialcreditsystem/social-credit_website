<template>
  <div id="app">
    <Stage class="section"/>
    <Intro class="section"/>
    <Types class="section"/>
  </div>
</template>

<script>
// Stylesheets
import "./style/main/fonts.scss";
import "./style/main/main.scss";

// Vue-Components
import Stage from "./components/Stage.vue";
import Intro from "./components/Intro.vue";
import Types from "./components/Types.vue";

export default {
  name: "app",
  components: {
    Stage,
    Intro,
    Types
  }
};
</script>
