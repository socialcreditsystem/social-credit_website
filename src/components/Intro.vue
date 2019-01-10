<template>
  <section class="intro" id="intro">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-7 col-12 intro__text-wrapper">
          <p class="section__paragraph__intro">
            The following visualization is based on a study by Prof. Dr. Genia Kostka. Would you like to learn more about the study?
            <a
              href="#"
              class="intro__link"
              data-toggle="modal"
              data-target="#SourceModal"
            >Learn more</a>.
          </p>

          <!-- Modal -->
          <div
            class="modal fade"
            id="SourceModal"
            tabindex="-1"
            role="dialog"
            aria-labelledby="exampleModalLabel"
            aria-hidden="true"
          >
            <div class="modal-dialog modal-full" role="document">
              <div class="modal-content">
                <div class="modal-header">
                  <a data-dismiss="modal" href="#intro">
                    <img src="../assets/black-arrow-back.svg">
                  </a>
                </div>
                <div class="modal-body">
                  <div class="container">
                    <div class="row justify-content-center">
                      <div class="col-9 intro">
                        <h2 class="section__heading__modal">
                          <span class="section__heading--bold">Data</span>
                          <span class="section__heading--light">&nbsp;source</span>
                        </h2>
                        <p
                          class="section__paragraph"
                        >We have used the study "China's Social Credit Systems and Public Opinion: Explaining High Levels of Approval" by Prof. Dr. Genia Kostka to create this visualization.</p>
                        <p class="section__paragraph">
                          The data has been retreived with an
                          <b>online survey</b> conducted between February and April 2018 with 2,209 respondents across China. Additionally, fifteen
                          <b>semi-structured interviews</b> were conducted with SCS users during March and July 2018 in Beijing and Shanghai.
                        </p>

                        <p class="section__paragraph">
                          The study tries to investigate the following aspects:
                          <br>1. Document the overall
                          <b>level of citizens’ (non-)approval</b> of different SCSs
                          <br>2. Identify the
                          <b>underlying factors</b> that drive variations in approval of SCSs
                        </p>

                        <p
                          class="section__paragraph"
                        >In the study, the participants were informed that the data would be anonymised. Nevertheless, the question arises as to whether the participants actually expressed their personal opinions. The effect on the studys results is considered marginal by the author.</p>

                        <p class="section__paragraph">
                          The whole study can be read on
                          <a
                            class="section__paragraph__link"
                            href="https://www.researchgate.net/publication/326625329_China%27s_Social_Credit_Systems_and_Public_Opinion_Explaining_High_Levels_of_Approval"
                            target="blank"
                          >ResearchGate</a>.
                        </p>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <h2 class="section__heading">
            <span class="section__heading--bold">Social Credit System</span>
            <span class="section__heading--light">&nbsp;What?</span>
          </h2>
          <p
            class="section__paragraph"
          >In recent years, China has made rapid advances in the incorporation of big data technologies in governance processes. In addition to using big data for more efficient policy making and enforcement, cutting-edge technologies are increasingly being used for social control and social management in order to address societal problems and pre-empt social instabilities. The emerging Social Credit System (SCS) stands out as an initiative with the potential to radically transform the state’s governance of both society and the economy. Under this system, individuals, businesses, social organisations and government agencies are assessed based on their ‘trustworthiness’.</p>
          <img
            class="section__image"
            src="https://picsum.photos/1400/1000"
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
  name: "Intro"
};
</script>
