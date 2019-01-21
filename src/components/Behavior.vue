<template>
  <section class="behavior" id="behavior">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-7 col-12 behavior__text-wrapper">
          <h2 class="section__heading">
            <span class="section__heading--light">Good and Bad</span>
            <span class="section__heading--bold">&nbsp;Behavior</span>
          </h2>
        </div>
      </div>
      <div class="row justify-content-center">
        <div class="col-lg-7 col-12 behavior__text-wrapper" style="text-align:center;">
          <p
            class="section__heading--light toogle__text--invisible toogle__label__left"
            id="label__commercial"
          >Commercial</p>

          <label class="switch">
            <input v-on:click="switchType()" type="checkbox" id="checkbox__scs__type" checked>
            <span class="slider round"></span>
          </label>
          <p
            class="section__heading--light toogle__label__right"
            id="label__governmental"
          >Governmental</p>
        </div>
      </div>

      <div id="governmental">
        <div class="row justify-content-center">
          <div class="col-lg-7 col-12 behavior__text-wrapper">
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
        <div class="row justify-content-center"></div>
        <div class="row justify-content-center" style="text-align: right">
          <div class="col-2" style="text-align: right">
            <p class="section__paragraph">
              <b>trustworthy</b> behavior
            </p>
          </div>

          <div class="col-3" style="text-align:right">
            <h2 class="list__element__heading">
              <span class="section__heading--bold">Red</span>
              <span class="section__heading--light">list</span>
            </h2>

            <img src="../assets/redlist.svg">
          </div>

          <div class="col-3" style="text-align:left">
            <h2 class="list__element__heading--black">
              <span class="section__heading--bold">Black</span>
              <span class="section__heading--light">list</span>
            </h2>
            <img src="../assets/blacklist.svg">
          </div>
          <div class="col-2" style="text-align: left">
            <p class="section__paragraph">
              <b>untrustworthy</b> or
              <b>illegal</b> behavior
            </p>
          </div>
        </div>
        <div class="row justify-content-center">
          <div class="col-4">
            <p
              class="section__paragraph"
              style="text-align: right"
            >Trustworthy people and companies are recorded on the redlist.</p>
          </div>

          <div class="col-4">
            <p
              class="section__paragraph"
              style="text-align: left"
            >Untrustworthy people and companies are recorded on the blacklist.</p>
          </div>
        </div>
        <div class="row justify-content-center">
          <div class="col-lg-8 col-12">
            <h4 class="consequences__element__subheading">
              <span class="section__heading--light">Possible</span>
              <span class="section__heading--bold">&nbsp;consequences</span>
            </h4>
            <ul class="consequences__element__list section__dashed-list">
              <li>Easier access to governmental services</li>
              <li>Tax reductions</li>
              <li>Limited access to high-speed trains and financal services</li>
            </ul>
          </div>
        </div>
      </div>
      <div id="commerical" class="toogle--hide">
        <div class="row justify-content-center">
          <div class="col-lg-7 col-12 behavior__text-wrapper">
            <p class="section__paragraph">
              How ones score is calculated differs between commercial social credit systems.For example, here is the relevant criterea at
              <b>Sesame Credit.</b>
            </p>
          </div>
        </div>

        <div class="row justify-content-center">
          <div class="col-lg-8 col-12">
            <h4 class="consequences__element__subheading">
              <span class="section__heading--light">Possible</span>
              <span class="section__heading--bold">&nbsp;consequences</span>
            </h4>
            <ul class="consequences__element__list section__dashed-list">
              <li>Qualification for personal credit loans</li>
              <li>Preferential treatment at hospitals and free health check-ups</li>
              <li>Fast-tracked visa applications</li>
              <li>Access to sharing economy services e. g. renting bikes or cars</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
// Stylesheets
import "../style/behavior/behavior.scss";
import { truncateWithEllipsis } from "@amcharts/amcharts4/.internal/core/utils/Utils";

export default {
  name: "Behavior",
  methods: {
    switchType() {
      let x = document.getElementById("checkbox__scs__type").checked;

      // Wenn in Checkbox Governmental ausgewählt ist
      if (x) {
        $("#commerical").addClass("toogle--hide");
        $("#governmental").removeClass("toogle--hide");

        $("#label__commercial").addClass("toogle__text--invisible");
        $("#label__governmental").removeClass("toogle__text--invisible");
        // Wenn in Checkbox Commercial ausgewählt ist
      } else {
        $("#governmental").addClass("toogle--hide");
        $("#commerical").removeClass("toogle--hide");

        $("#label__governmental").addClass("toogle__text--invisible");
        $("#label__commercial").removeClass("toogle__text--invisible");
      }
    }
  }
};
</script>
