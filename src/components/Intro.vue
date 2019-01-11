<template>
  <section class="intro" id="intro">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-7 col-12 intro__text-wrapper">
          <div class="intro__study-info row justify-content-center align-items-center">
            <img src="../assets/info-circle.svg" alt="Info" class="intro__study-info__icon col-1">
            <div class="intro__study-info__text col-11">
              The following visualization is based on a study by Prof. Dr. Genia Kostka. Would you like to learn more about the study?
              <a
                v-on:click="showSource"
                class="intro__study-info__text--link"
              >Learn more</a>.
            </div>
          </div>
          <h2 class="section__heading">
            <span class="section__heading--bold">Social Credit System</span>
            <span class="section__heading--light">&nbsp;What?</span>
          </h2>
          <p
            class="section__paragraph intro__paragraph"
          >In recent years, China has made rapid advances in the incorporation of big data technologies in governance processes. In addition to using big data for more efficient policy making and enforcement, cutting-edge technologies are increasingly being used for social control and social management in order to address societal problems and pre-empt social instabilities. The emerging Social Credit System (SCS) stands out as an initiative with the potential to radically transform the state’s governance of both society and the economy. Under this system, individuals, businesses, social organisations and government agencies are assessed based on their ‘trustworthiness’.</p>
          <img
            class="section__image"
            src="../assets/imgs/surveillance.png"
            alt="Chinese people being rated by a camera software (symbolic picture)"
          >
        </div>
      </div>
    </div>
  </section>
</template>

<script>
// Stylesheets
import "../style/intro/intro.scss";

export default {
  name: "Intro",
  methods: {
    showSource: function() {
      document.getElementById("dataSource").style.left = 0;
      document.body.style.overflow = "hidden";
    }
  }
};
</script>
