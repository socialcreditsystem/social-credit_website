<template>
  <div id="app">
    <Navigation/>
    <Stage class="section"/>
    <Intro class="section"/>
    <Source class="section"/>
    <Types class="section"/>
    <Dissemination class="section"/>
    <Conclusion class="section"/>
  </div>
</template>

<script>
// Stylesheets
import "./style/main/fonts.scss";
import "./style/main/main.scss";

// Vue-Components
import Navigation from "./components/Navigation.vue";
import Stage from "./components/Stage.vue";
import Intro from "./components/Intro.vue";
import Source from "./components/Source.vue";
import Types from "./components/Types.vue";
import Dissemination from "./components/Dissemination.vue";
import Conclusion from "./components/Conclusion.vue";

export default {
  name: "app",
  components: {
    Stage,
    Navigation,
    Intro,
    Source,
    Types,
    Dissemination,
    Conclusion
  }
};
</script>
