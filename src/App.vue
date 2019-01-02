<template>
  <div id="app">
    <Stage class="section"/>
    <Intro class="section"/>
  </div>
</template>

<script>
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

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
.section {
  padding: 50px 0;
}
.section__heading {
}
.section__heading--bold {
}
.section__heading--light {
}
.section__paragraph {
}
.section__image {
  width: 100%;
}
</style>
