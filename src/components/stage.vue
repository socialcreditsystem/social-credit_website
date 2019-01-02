<template>
  <section class="d-flex align-items-end stage">
    <div class="stage__headline">
      <h3>Seen through Chinese eyes</h3>
      <h1>China's<br/>Social Credit System</h1>
      <h6>A visualization by the students Benedikt Asal, Philipp Danne, Selina Groß and David Wostracky of the Online Media course of studies at Baden-Württemberg Cooperative State University Mosbach.</h6>
    </div>
  </section>
</template>

<script>
export default {
  name: "Stage"
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.stage {
  background: #333;
  min-height: 100vh;
  color: #ffffff;
}
.stage__headline {
  margin-bottom: 0;
  display: inline-block;
  vertical-align: bottom;
}
</style>
