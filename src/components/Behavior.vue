<template>
  <section class="behavior" id="behavior">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-7 col-12 behavior__text-wrapper">
          <h2 class="section__heading">
            <span class="section__heading--light">Good and Bad</span>
            <span class="section__heading--bold">&nbsp;Behavior</span>
          </h2>
          <p class="section__paragraph">
            Governments publish
            <b>redlists</b> and
            <b>blacklists</b> for individuals and organizations with trustworthy / untrustworthy or illegal behavior.
          </p>
        </div>
      </div>
      <div class="row justify-content-center" style="text-align: left">
        <div class="col-4">
          <img src="../assets/arrow-redlist.svg">
        </div>

        <div class="col-4" style="text-align:right">
          <img src="../assets/arrow-blacklist.svg">
        </div>
      </div>

      <div class="row justify-content-center" style="text-align: right">
        <div class="col-6">
          <img src="../assets/redlist.svg">
        </div>

        <div class="col-6" style="text-align:left">
          <img src="../assets/blacklist.svg">
        </div>
      </div>
      <div class="row justify-content-center">
        <div class="col-4">
          <p class="section__paragraph" style="text-align: right">
            By doing something on the redlist your
            <b>score gets higher.</b>
          </p>
        </div>

        <div class="col-4">
          <p class="section__paragraph" style="text-align: left">
            By doing something on the blacklist
            your
            <b>score gets lower.</b>
          </p>
        </div>
      </div>
      <div class="row justify-content-center">
        <div class="col-lg-7 col-12">
          <h4
            class="consequences__element__subheading"
          >Possible consequences affected by your score:</h4>
          <ul class="consequences__element__list">
            <li>Tax reductions</li>
            <li>Easier access to governmental services</li>
            <li>Limited access to high-speed trains and financal services</li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
// Stylesheets
import "../style/behavior/behavior.scss";

export default {
  name: "Behavior"
};
</script>
