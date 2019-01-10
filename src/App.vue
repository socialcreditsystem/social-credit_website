<template>
  <div id="app">
    <Navigation/>
    <Stage class="section"/>
    <Intro class="section"/>
    <Source class="additional_information" id="dataSource"/>
    <Types class="section"/>
    <Behavior class="section"/>
    <Dissemination class="section"/>
    <Approval class="section"/>
    <Country class="section"/>
    <RualUrban class="section"/>
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
import Types from "./components/Types.vue";
import Approval from "./components/Approval.vue";
import Source from "./components/Source.vue";
import Behavior from "./components/Behavior.vue";
import Dissemination from "./components/Dissemination.vue";
import Country from "./components/Country.vue";
import RualUrban from "./components/RualUrban.vue";
import Conclusion from "./components/Conclusion.vue";

export default {
  name: "app",
  components: {
    Stage,
    Navigation,
    Intro,
    Approval,
    Source,
    Types,
    Behavior,
    Dissemination,
    Country,
    RualUrban,
    Conclusion
  }
};
</script>
