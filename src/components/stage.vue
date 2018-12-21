<template>
  <div class="d-flex align-items-end stage">
    <div class="stage--intro-text">
      <h1>{{ title }}</h1>
    </div>
  </div>
</template>

<script>
export default {
  name: "Stage",
  props: {
    title: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.stage {
  background: #333;
  height: 100vh;
  padding: 20px;
  color: #ffffff;
}
.stage--intro-text {
  margin-bottom: 0;
  display: inline-block;
  vertical-align: bottom;
}
</style>
