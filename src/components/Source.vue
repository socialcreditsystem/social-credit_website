<template>
  <section class="source">
    <div v-on:click="hideSource" class="source__back-button">
      <img src="../assets/black-arrow-back.svg" alt="Back" class="source__back-button--icon">
    </div>
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-8 source">
          <h2 class="section__heading">
            <span class="section__heading--bold">Data</span>
            <span class="section__heading--light">&nbsp;source</span>
          </h2>
          <p
            class="section__paragraph section__data__paragraph"
          >We have used the study "China's Social Credit Systems and Public Opinion: Explaining High Levels of Approval" by Prof. Dr. Genia Kostka to create this visualization.</p>
          <p class="section__paragraph section__data__paragraph">
            The data has been retreived with an
            <b>online survey</b> conducted between February and April 2018 with 2,209 respondents across China. Additionally, fifteen
            <b>semi-structured interviews</b> were conducted with SCS users during March and July 2018 in Beijing and Shanghai.
          </p>

          <p class="section__paragraph section__data__paragraph">
            The study tries to investigate the following aspects:
            <br>1. Document the overall
            <b>level of citizens’ (non-)approval</b> of different SCS
            <br>2. Identify the
            <b>underlying factors</b> that drive variations in approval of SCS
          </p>

          <p
            class="section__paragraph section__data__paragraph"
          >In the study, the participants were informed that the data would be anonymised. Nevertheless, the question arises as to whether the participants actually expressed their personal opinions. The effect on the studys results is considered marginal by the author.</p>

          <p class="section__paragraph section__data__paragraph">
            The whole study can be read on
            <a
              class="section__paragraph__link section__data__paragraph"
              href="https://www.researchgate.net/publication/326625329_China%27s_Social_Credit_Systems_and_Public_Opinion_Explaining_High_Levels_of_Approval"
              target="blank"
            >ResearchGate</a>.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
// Stylesheets
import "../style/source/source.scss";

export default {
  name: "Source",
  methods: {
    hideSource: function() {
      document.getElementById("dataSource").style.left = "100%";
      document.body.style.overflow = "auto";
    }
  }
};
</script>
