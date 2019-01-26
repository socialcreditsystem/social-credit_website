<template>
  <section class="dissemination" id="dissemination">
    <div class="container wow slideInUp" data-wow-duration="2s">
      <div class="row justify-content-center">
        <div class="col-lg-7 col-12 dissemination__text-wrapper">
          <h2 class="section__heading section__heading--color--light">
            <span class="section__heading--bold">Distribution</span>
            <span class="section__heading--light">&nbsp;of SCS</span>
          </h2>
          <p
            class="section__paragraph section__paragraph--color--light"
          >Most participants of the study report that they take part in a commercial social credit system. 19 % of them in the two most popular ones - Sesame Credit and Tencent Credit.</p>
        </div>
        <div id="disseminationChart" ref="disseminationChart"></div>
      </div>
    </div>
  </section>
</template>

<script>
// Stylesheets
import * as am4core from "@amcharts/amcharts4/core";
import * as am4charts from "@amcharts/amcharts4/charts";
import am4themes_animated from "@amcharts/amcharts4/themes/animated";
am4core.useTheme(am4themes_animated);

import "../style/dissemination/dissemination.scss";

export default {
  name: "Dissemination",
  mounted() {
    let chart = am4core.create("disseminationChart", am4charts.RadarChart);
    // Add data

    chart.data = [
      {
        category: "Government PilotResearch",
        value: 7.4,
        full: 100
      },
      {
        category: "I don't know",
        value: 8.18,
        full: 100
      },
      {
        category: "I do not take part in any social credit system",
        value: 16.47,
        full: 100
      },
      {
        category: "Tencent Credit",
        value: 30.6,
        full: 100
      },
      {
        category: "Sesame Credit",
        value: 58.18,
        full: 100
      },
      {
        category: "Commercial Credit System",
        value: 80.04,
        full: 100
      }
    ];

    // Make chart not full circle
    chart.startAngle = -90;
    chart.endAngle = 180;
    chart.innerRadius = am4core.percent(20);

    // Set number format
    chart.numberFormatter.numberFormat = "#.#'%'";

    // Create axes
    let categoryAxis = chart.yAxes.push(new am4charts.CategoryAxis());
    categoryAxis.dataFields.category = "category";

    categoryAxis.renderer.grid.template.location = 0;
    categoryAxis.renderer.grid.template.strokeOpacity = 0;
    categoryAxis.renderer.labels.template.horizontalCenter = "right";
    categoryAxis.renderer.labels.template.fontWeight = 500;
    categoryAxis.renderer.labels.template.adapter.add("fill", function(
      fill,
      target
    ) {
      return target.dataItem.index >= 0
        ? chart.colors.getIndex(target.dataItem.index)
        : fill;
    });
    categoryAxis.renderer.minGridDistance = 10;

    let valueAxis = chart.xAxes.push(new am4charts.ValueAxis());
    valueAxis.renderer.grid.template.strokeOpacity = 0;

    valueAxis.min = 0;
    valueAxis.max = 100;
    valueAxis.strictMinMax = true;
    // Prozentangaben
    valueAxis.renderer.labels.template.fill = am4core.color("#ffffff");

    chart.colors.list = [
      am4core.color("#3B4C81").lighten(0.2),
      am4core.color("#757575"),
      am4core.color("#757575").lighten(0.2),
      am4core.color("#EF5440").lighten(-0.16),
      am4core.color("#EF5440").lighten(-0.08),
      am4core.color("#EF5440")
    ];

    // Create series
    let series1 = chart.series.push(new am4charts.RadarColumnSeries());
    series1.dataFields.valueX = "full";
    series1.dataFields.categoryY = "category";
    series1.clustered = false;
    series1.columns.template.fill = new am4core.InterfaceColorSet().getFor(
      "alternativeBackground"
    );
    series1.columns.template.fillOpacity = 0.08;
    series1.columns.template.cornerRadiusTopLeft = 20;
    series1.columns.template.strokeWidth = 0;
    series1.columns.template.radarColumn.cornerRadius = 20;

    let series2 = chart.series.push(new am4charts.RadarColumnSeries());
    series2.dataFields.valueX = "value";
    series2.dataFields.categoryY = "category";
    series2.clustered = false;
    series2.columns.template.strokeWidth = 0;
    series2.columns.template.tooltipText = "{category}: [bold]{value}[/]";
    series2.columns.template.radarColumn.cornerRadius = 20;

    series2.sequencedInterpolation = false;
    series2.defaultState.transitionDuration = 2500;

    series2.columns.template.adapter.add("fill", function(fill, target) {
      return chart.colors.getIndex(target.dataItem.index);
    });
  }
};
</script>
