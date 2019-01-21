
 <script src="https://www.amcharts.com/lib/4/core.js"></script>
    <script src="https://www.amcharts.com/lib/4/charts.js"></script>
    <script src="https://www.amcharts.com/lib/4/themes/animated.js"></script>
<template>
  <section class="rualurban" id="rualurban">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-7 col-12 rualurban__text-wrapper">
          <p
            class="section__paragraph section__paragraph--color--light"
          >But what specific effects have Chinese citizens of the city and the countryside experienced? The chart below illustrates the differences between urban and rural areas.</p>
        </div>
      </div>
      <div class="row justify-content-center">
        <div class="col-md-4 col-12 rural__image-wrapper">
          <div class="rualurban__image-wrapper">
            <img src="../assets/house-rural.svg">
            <br>
            <p class="section__paragraph section__paragraph--color--light">
              <span class="rural__element__subheading">Rural</span>
              <span class="element__subheading">&nbsp;area</span>
            </p>
          </div>
        </div>
        <div class="col-md-4 col-12 urban__image-wrapper">
          <div class="rualurban__image-wrapper">
            <img src="../assets/house-city.svg">
            <br>
            <p class="section__paragraph section__paragraph--color--light">
              <span class="urban__element__subheading">Urban</span>
              <span class="element__subheading">&nbsp;area</span>
            </p>
          </div>
        </div>
      </div>

      <div class="row justify-content-center">
        <div class="col-5 section__paragraph--left">
          <p
            class="section__paragraph section__paragraph--color--light text-right"
          >Obtained credit without difficulties</p>
        </div>
        <div class="col-5">
          <div class="ruralurban0 ruralurban__diagramm" ref="ruralurban0"></div>
        </div>
      </div>

      <div class="row justify-content-center">
        <div class="col-5 section__paragraph--left">
          <p
            class="section__paragraph section__paragraph--color--light text-right"
          >Obtained credit with difficulties</p>
        </div>
        <div class="col-5">
          <div class="ruralurban1 ruralurban__diagramm" ref="ruralurban1"></div>
        </div>
      </div>

      <div class="row justify-content-center">
        <div class="col-5 section__paragraph--left">
          <p
            class="section__paragraph section__paragraph--color--light text-right"
          >Received lower interest rates on loans from my bank</p>
        </div>
        <div class="col-5">
          <div class="ruralurban2 ruralurban__diagramm" ref="ruralurban2"></div>
        </div>
      </div>

      <div class="row justify-content-center">
        <div class="col-5 section__paragraph--left">
          <p
            class="section__paragraph section__paragraph--color--light text-right"
          >Received higher interest rates on savings from my bank</p>
        </div>
        <div class="col-5">
          <div class="ruralurban3 ruralurban__diagramm" ref="ruralurban3"></div>
        </div>
      </div>

      <div class="row justify-content-center">
        <div class="col-5 section__paragraph--left">
          <p
            class="section__paragraph section__paragraph--color--light text-right"
          >Received a fast-tracked visa</p>
        </div>
        <div class="col-5">
          <div class="ruralurban4 ruralurban__diagramm" ref="ruralurban4"></div>
        </div>
      </div>

      <div class="row justify-content-center">
        <div class="col-5 section__paragraph--left">
          <p
            class="section__paragraph section__paragraph--color--light text-right"
          >Used deposit-free sharing economy services (such as a rental bike or car)</p>
        </div>
        <div class="col-5">
          <div class="ruralurban5 ruralurban__diagramm" ref="ruralurban5"></div>
        </div>
      </div>

      <div class="row justify-content-center">
        <div class="col-5 section__paragraph--left">
          <p
            class="section__paragraph section__paragraph--color--light text-right"
          >Used fast-tracked check-ins for hotels or flights</p>
        </div>
        <div class="col-5">
          <div class="ruralurban6 ruralurban__diagramm" ref="ruralurban6"></div>
        </div>
      </div>

      <div class="row justify-content-center">
        <div class="col-5 section__paragraph--left">
          <p
            class="section__paragraph section__paragraph--color--light text-right"
          >Experienced a positive impact on my online dating</p>
        </div>
        <div class="col-5">
          <div class="ruralurban7 ruralurban__diagramm" ref="ruralurban7"></div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import "../style/rualurban/rualurban.scss";

/* Imports */
import * as am4core from "@amcharts/amcharts4/core";
import * as am4charts from "@amcharts/amcharts4/charts";
import am4themes_animated from "@amcharts/amcharts4/themes/animated";

am4core.useTheme(am4themes_animated);
// Themes end

export default {
  name: "RualUrban",
  mounted() {
    let data_urban = ["37", "2", "18", "11", "14", "40", "35", "4"];
    let data_rural = ["31", "5", "12", "9", "11", "32", "28", "4"];

    for (let i = 0; i < 8; i++) {
      // Create chart instance
      let chart = am4core.create("ruralurban" + i, am4charts.XYChart);

      chart.creditsPosition = "bottom-right";
      // Add data
      chart.data = [
        {
          location: "Urban",
          percentage: data_urban[i],
          color: am4core.color("#D5433D")
        },
        {
          location: "Rural",
          percentage: data_rural[i],
          color: am4core.color("#3B4C81")
        }
      ];

      // Create axes
      let categoryAxis = chart.yAxes.push(new am4charts.CategoryAxis());
      categoryAxis.dataFields.category = "location";
      categoryAxis.renderer.grid.template.disabled = true;
      categoryAxis.renderer.minGridDistance = 30;
      categoryAxis.renderer.labels.template.disabled = true;
      categoryAxis.renderer.labels.template.fontSize = 20;

      let valueAxis = chart.xAxes.push(new am4charts.ValueAxis());
      valueAxis.renderer.grid.template.strokeDasharray = "4,4";
      valueAxis.renderer.labels.template.disabled = true;
      valueAxis.min = 0;
      valueAxis.max = 40;

      // Do not crop bullets
      chart.maskBullets = false;
      // Remove padding
      chart.paddingBottom = 0;

      // Change credit position
      chart.logo.align = "right";
      chart.logo.valign = "bottom";

      // Create series
      let series = chart.series.push(new am4charts.ColumnSeries());
      series.dataFields.valueX = "percentage";
      series.dataFields.categoryY = "location";
      series.columns.template.propertyFields.fill = "color";
      series.columns.template.propertyFields.stroke = "color";

      // Create Percentage
      let percentageLabel = series.bullets.push(new am4charts.LabelBullet());
      percentageLabel.label.text = "{valueX}%";

      percentageLabel.label.dx = 30;
      percentageLabel.label.truncate = false;
      percentageLabel.label.hideOversized = false;
      percentageLabel.label.fill = am4core.color("#fff");
    }
  }
};
</script>
