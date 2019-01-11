
 <script src="https://www.amcharts.com/lib/4/core.js"></script>
    <script src="https://www.amcharts.com/lib/4/charts.js"></script>
    <script src="https://www.amcharts.com/lib/4/themes/animated.js"></script>
<template>
  <section class="country" id="cityvscountry">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-7 col-12 country__text-wrapper">
          <h2 class="section__heading section__heading--color--light">
            <span class="section__heading--bold">City</span>
            <span class="section__heading--light">&nbsp;vs.</span>
            <span class="section__heading--bold">&nbsp;Countryside</span>
          </h2>
        </div>
      </div>
    </div>
    <div class="parallaxcountry">
      <div class="parallax--right">
        <p
          class="parallax__paragraph paragraph--light"
        >The findings show, further, that there is less approval for SCSs in rural areas. One potential explanation is that respondents in rural areas are less familiar with SCSs and hence more sceptical.</p>
      </div>
      <div class="parallax--left">
        <p
          class="parallax__paragraph paragraph--light"
        >For example, 43% citizens from the countryside report that they don't know how their score is calculated. But 87% have already received benefits by participating in a commercial SCS pilot.</p>
      </div>
    </div>
    <div class="parallaxcountry"></div>
    <div class="parallaxcity">
      <div class="parallax--right">
        <p
          class="parallax__paragraph paragraph--dark"
        >In contrast to that, the knowledge about how the own score is calculated is higher for citizens from the urban area. Only 36% do not know how the score is calculated. This is 7% less than in rural areas.</p>
      </div>
    </div>
    <div class="parallaxcity">
      <div class="parallax--left">
        <p
          class="parallax__paragraph paragraph--dark"
        >The number of people who have already received benefits from participating in a commercial SCS is almost the same in the city. Only one percent more report that they have received benefits (88%).</p>
      </div>
    </div>
    <div class="parallaxcity"></div>
  </section>
</template>

<script>
import "../style/country/country.scss";

export default {
  name: "Country"
};
</script>
