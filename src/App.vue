<template>
  <div id="app">
    <Stage class="section"/>
    <Intro class="section"/>
  </div>
</template>

<script>
// Stylesheets
import "./style/main/fonts.scss";
import "./style/main/main.scss";

// Vue-Components
import Stage from "./components/Stage.vue";
import Intro from "./components/Intro.vue";

export default {
  name: "app",
  components: {
    Stage,
    Intro
  }
};
</script>
