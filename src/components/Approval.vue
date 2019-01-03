<template>
    <section class="approval">
        <div class="container">
            <div class="row justify-content-center">
                <div class="col-8 approval__intro">
                    <h2 class="section__heading"><span class="section__heading--bold">Approval</span><span class="section__heading--light"> of SCS</span></h2>
                    <p class="section__paragraph">Regardless of their demographics, most Chinese strongly approve or somewhat approve the SCSs. But the degree of approval varies across age, income, gender, education and region. Let’s explore the differences in the following charts.</p>
                </div>
            </div>
            <div class="row justify-content-end">
                <div class="col-11 approval__chart" ref="chartdiv"></div>
            </div>
        </div>
    </section>
</template>

<script>
// Stylesheets
import "../style/approval/approval.scss";

/* Imports */
import * as am4core from "@amcharts/amcharts4/core";
import * as am4charts from "@amcharts/amcharts4/charts";
import am4themes_animated from "@amcharts/amcharts4/themes/animated";

function am4themes_approvalTheme(target) {
  if (target instanceof am4charts.AxisLabel) {
    target.fill = am4core.color("#fff");
  }
  if (target instanceof am4core.ColorSet) {
    target.list = [
      am4core.color("#273150"),
      am4core.color("#3B4C81"),
      am4core.color("#777777"),
      am4core.color("#D5433D"),
      am4core.color("#BF3C37")
    ];
  }
}

/* Chart code */
// Themes begin
am4core.useTheme(am4themes_animated);
am4core.useTheme(am4themes_approvalTheme);
// Themes end

export default {
  name: "Approval",
  mounted() {
    let chart = am4core.create(this.$refs.chartdiv, am4charts.XYChart);
    chart.hiddenState.properties.opacity = 0; // this creates initial fade-in

    chart.data = [
      {
        category: "14-30 years",
        stronglyDisapprove: 6.8,
        somewhatDisapprove: 5.2,
        neutral: 15,
        somewhatApprove: 40,
        stronglyApprove: 30
      },
      {
        category: "31-50 years",
        stronglyDisapprove: 6.8,
        somewhatDisapprove: 5.2,
        neutral: 15,
        somewhatApprove: 40,
        stronglyApprove: 30
      },
      {
        category: "51-65 years",
        stronglyDisapprove: 6.8,
        somewhatDisapprove: 5.2,
        neutral: 15,
        somewhatApprove: 40,
        stronglyApprove: 30
      }
    ];

    chart.colors.step = 1;
    chart.padding(30, 30, 10, 30);
    chart.legend = new am4charts.Legend();
    chart.legend.position = "right";
    chart.legend.width = am4core.percent(60);
    chart.legend.labels.template.text = "[white]{name}[/]";

    let categoryAxis = chart.xAxes.push(new am4charts.CategoryAxis());
    categoryAxis.dataFields.category = "category";
    categoryAxis.renderer.grid.template.location = 0;
    categoryAxis.renderer.grid.template.stroke = am4core.color("#fff");

    let valueAxis = chart.yAxes.push(new am4charts.ValueAxis());
    valueAxis.min = 0;
    valueAxis.max = 100;
    valueAxis.strictMinMax = true;
    valueAxis.calculateTotals = true;
    valueAxis.renderer.minWidth = 50;
    valueAxis.renderer.grid.template.stroke = am4core.color("#fff");

    let series1 = chart.series.push(new am4charts.ColumnSeries());
    series1.columns.template.width = am4core.percent(80);
    series1.columns.template.tooltipText =
      "{name}: {valueY.totalPercent.formatNumber('#.00')}%";
    series1.name = "strongly disapprove";
    series1.dataFields.categoryX = "category";
    series1.dataFields.valueY = "stronglyDisapprove";
    series1.dataFields.valueYShow = "totalPercent";
    series1.dataItems.template.locations.categoryX = 0.5;
    series1.stacked = true;
    series1.tooltip.pointerOrientation = "vertical";

    let bullet1 = series1.bullets.push(new am4charts.LabelBullet());
    bullet1.label.text = "{valueY.totalPercent.formatNumber('#.00')}%";
    bullet1.label.fill = am4core.color("#ffffff");
    bullet1.locationY = 0.5;

    let series2 = chart.series.push(new am4charts.ColumnSeries());
    series2.columns.template.width = am4core.percent(80);
    series2.columns.template.tooltipText =
      "{name}: {valueY.totalPercent.formatNumber('#.00')}%";
    series2.name = "somewhat disapprove";
    series2.dataFields.categoryX = "category";
    series2.dataFields.valueY = "somewhatDisapprove";
    series2.dataFields.valueYShow = "totalPercent";
    series2.dataItems.template.locations.categoryX = 0.5;
    series2.stacked = true;
    series2.tooltip.pointerOrientation = "vertical";

    let bullet2 = series2.bullets.push(new am4charts.LabelBullet());
    bullet2.label.text = "{valueY.totalPercent.formatNumber('#.00')}%";
    bullet2.locationY = 0.5;
    bullet2.label.fill = am4core.color("#ffffff");

    let series3 = chart.series.push(new am4charts.ColumnSeries());
    series3.columns.template.width = am4core.percent(80);
    series3.columns.template.tooltipText =
      "{name}: {valueY.totalPercent.formatNumber('#.00')}%";
    series3.name = "neither disapprove nor approve";
    series3.dataFields.categoryX = "category";
    series3.dataFields.valueY = "neutral";
    series3.dataFields.valueYShow = "totalPercent";
    series3.dataItems.template.locations.categoryX = 0.5;
    series3.stacked = true;
    series3.tooltip.pointerOrientation = "vertical";

    let bullet3 = series3.bullets.push(new am4charts.LabelBullet());
    bullet3.label.text = "{valueY.totalPercent.formatNumber('#.00')}%";
    bullet3.locationY = 0.5;
    bullet3.label.fill = am4core.color("#ffffff");

    let series4 = chart.series.push(new am4charts.ColumnSeries());
    series4.columns.template.width = am4core.percent(80);
    series4.columns.template.tooltipText =
      "{name}: {valueY.totalPercent.formatNumber('#.00')}%";
    series4.name = "somewhat approve";
    series4.dataFields.categoryX = "category";
    series4.dataFields.valueY = "somewhatApprove";
    series4.dataFields.valueYShow = "totalPercent";
    series4.dataItems.template.locations.categoryX = 0.5;
    series4.stacked = true;
    series4.tooltip.pointerOrientation = "vertical";

    let bullet4 = series4.bullets.push(new am4charts.LabelBullet());
    bullet4.label.text = "{valueY.totalPercent.formatNumber('#.00')}%";
    bullet4.locationY = 0.5;
    bullet4.label.fill = am4core.color("#ffffff");

    let series5 = chart.series.push(new am4charts.ColumnSeries());
    series5.columns.template.width = am4core.percent(80);
    series5.columns.template.tooltipText =
      "{name}: {valueY.totalPercent.formatNumber('#.00')}%";
    series5.name = "strongly  approve";
    series5.dataFields.categoryX = "category";
    series5.dataFields.valueY = "stronglyApprove";
    series5.dataFields.valueYShow = "totalPercent";
    series5.dataItems.template.locations.categoryX = 0.5;
    series5.stacked = true;
    series5.tooltip.pointerOrientation = "vertical";

    let bullet5 = series5.bullets.push(new am4charts.LabelBullet());
    bullet5.label.text = "{valueY.totalPercent.formatNumber('#.00')}%";
    bullet5.locationY = 0.5;
    bullet5.label.fill = am4core.color("#ffffff");
  }
};
</script>
