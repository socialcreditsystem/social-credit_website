<template>
  <section class="country" id="cityvscountry">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-6 col-12 country__text-wrapper">
          <div class="section__heading__container">
            <h2 class="section__heading section__heading--color--light">
              <span class="section__heading--bold">City</span>
              <span class="section__heading--light">&nbsp;vs.</span>
              <span class="section__heading--bold">&nbsp;Countryside</span>
            </h2>
          </div>
        </div>
      </div>
    </div>
    <div class="parallaxcountry">
      <div class="container">
        <div class="row justify-content-center">
          <div class="col-lg-6 col-12">
            <div class="parallax--divider--top"></div>
            <p
              class="parallax__paragraph"
            >The findings show, further, that there is less approval for SCSs in rural areas. One potential explanation is that respondents in rural areas are less familiar with SCSs and hence more sceptical.</p>

            <div class="parallax--divider"></div>
            <p
              class="parallax__paragraph"
            >For example, 43% citizens from the countryside report that they don't know how their score is calculated. But 87% have already received benefits by participating in a commercial SCS pilot.</p>
            <div class="parallax--divider--bottom"></div>
          </div>
        </div>
      </div>
    </div>

    <div class="parallaxcity">
      <div class="container">
        <div class="row justify-content-center">
          <div class="col-lg-6 col-12">
            <div class="parallax--divider--top"></div>
            <p
              class="parallax__paragraph"
            >In contrast to that, the knowledge about how the own score is calculated is higher for citizens from the urban area. Only 36% do not know how the score is calculated. This is 7% less than in rural areas.</p>

            <div class="parallax--divider"></div>
            <p
              class="parallax__paragraph"
            >The number of people who have already received benefits from participating in a commercial SCS is almost the same in the city. Only one percent more report that they have received benefits (88%).</p>
            <div class="parallax--divider--bottom"></div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import "../style/country/country.scss";

export default {
  name: "Country"
};
</script>
