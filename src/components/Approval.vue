<template>
    <section class="approval">
        <div class="container">
            <div class="row justify-content-center">
                <div class="col-8 approval__intro">
                    <h2 class="section__heading"><span class="section__heading--bold">Approval</span><span class="section__heading--light"> of SCS</span></h2>
                    <p class="section__paragraph">Regardless of their demographics, most Chinese strongly approve or somewhat approve the SCSs. But the degree of approval varies across age, income, gender, education and region. Let’s explore the differences in the following charts.</p>
                </div>
            </div>
            <div class="row justify-content-center">
                <div class="col-8 approval__controls">
                    <ul class="approval__controls__element">
                        <!-- <li v-on:click="changeToOverall">Overall</li> -->
                        <li v-on:click="changeToAge" id="changeToAge" class="approval__controls__element__group approval__controls__element__group--default"><img class="approval__controls__element__icons approval__controls__element__icons--default" src="../assets/filter-age.svg"/><span class="approval__controls__element__label approval__controls__element__label--default">Age</span></li>
                        <li v-on:click="changeToGender" id="changeToGender" class="approval__controls__element__group"><img class="approval__controls__element__icons" src="../assets/filter-gender.svg"/><span class="approval__controls__element__label">Gender</span></li>
                        <li v-on:click="changeToEducation" id="changeToEducation" class="approval__controls__element__group"><img class="approval__controls__element__icons" src="../assets/filter-education.svg"/><span class="approval__controls__element__label">Education</span></li>
                        <li v-on:click="changeToIncome" id="changeToIncome" class="approval__controls__element__group"><img class="approval__controls__element__icons" src="../assets/filter-income.svg"/><span class="approval__controls__element__label">Income</span></li>
                        <li v-on:click="changeToLocation" id="changeToLocation" class="approval__controls__element__group"><img class="approval__controls__element__icons" src="../assets/filter-location.svg"/><span class="approval__controls__element__label">Location</span></li>
                        <li v-on:click="changeToRegion" id="changeToRegion" class="approval__controls__element__group"><img class="approval__controls__element__icons" src="../assets/filter-region.svg"/><span class="approval__controls__element__label">Region</span></li>
                    </ul>
                </div>
            </div>
            <h3 class="approval__controls__heading" id="approvalHeading">Age</h3>
            <div class="row justify-content-end">
                <div class="col-11 approval__chart" ref="chartdiv"></div>
            </div>
        </div>
    </section>
</template>

<script>
// Stylesheets
import "../style/approval/approval.scss";

function changeToCategory(id, categoryName) {
  var elements = document.querySelectorAll(
    ".approval__controls__element__group"
  );
  for (var i = 0; i < elements.length; i++) {
    elements[i].style.opacity = 0.5;
  }

  document.getElementById(id).style.opacity = 1;
  document.getElementById("approvalHeading").innerText = categoryName;
}

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

let chart;

export default {
  name: "Approval",
  methods: {
    changeToOverall: function() {
      chart.data = [
        {
          category: "Overall",
          stronglyDisapprove: 0.6,
          somewhatDisapprove: 0.8,
          neutral: 18.7,
          somewhatApprove: 31.1,
          stronglyApprove: 48.9
        }
      ];
    },
    changeToAge: function() {
      changeToCategory("changeToAge", "Age");
      chart.data = [
        {
          category: "14-30 years",
          stronglyDisapprove: 6.8,
          somewhatDisapprove: 7.2,
          neutral: 19.9,
          somewhatApprove: 33.6,
          stronglyApprove: 45.1
        },
        {
          category: "31-50 years",
          stronglyDisapprove: 0.5,
          somewhatDisapprove: 0.5,
          neutral: 17.0,
          somewhatApprove: 28.5,
          stronglyApprove: 53.4
        },
        {
          category: "51-65 years",
          stronglyDisapprove: 0,
          somewhatDisapprove: 4.3,
          neutral: 18.4,
          somewhatApprove: 21.0,
          stronglyApprove: 56.4
        }
      ];
    },
    changeToGender: function() {
      changeToCategory("changeToGender", "Gender");
      chart.data = [
        {
          category: "female",
          stronglyDisapprove: 0.6,
          somewhatDisapprove: 0.9,
          neutral: 19.5,
          somewhatApprove: 33.8,
          stronglyApprove: 45.3
        },
        {
          category: "male",
          stronglyDisapprove: 0.6,
          somewhatDisapprove: 0.7,
          neutral: 18.1,
          somewhatApprove: 29.5,
          stronglyApprove: 51.2
        }
      ];
    },
    changeToEducation: function() {
      changeToCategory("changeToEducation", "Education");
      chart.data = [
        {
          category: "no",
          stronglyDisapprove: 3.5,
          somewhatDisapprove: 0,
          neutral: 57.2,
          somewhatApprove: 18.2,
          stronglyApprove: 21.0
        },
        {
          category: "low",
          stronglyDisapprove: 1.5,
          somewhatDisapprove: 1.8,
          neutral: 35.9,
          somewhatApprove: 25.9,
          stronglyApprove: 35.0
        },
        {
          category: "medium",
          stronglyDisapprove: 0.0,
          somewhatDisapprove: 0.6,
          neutral: 21.6,
          somewhatApprove: 36.7,
          stronglyApprove: 41.2
        },
        {
          category: "high",
          stronglyDisapprove: 0.4,
          somewhatDisapprove: 0.6,
          neutral: 12.7,
          somewhatApprove: 31.6,
          stronglyApprove: 54.8
        }
      ];
    },
    changeToIncome: function() {
      changeToCategory("changeToIncome", "Income");
      chart.data = [
        {
          category: "less than 1000 RMB",
          stronglyDisapprove: 0.7,
          somewhatDisapprove: 0.6,
          neutral: 29.1,
          somewhatApprove: 28.8,
          stronglyApprove: 40.9
        },
        {
          category: "1000 - 4000 RMB",
          stronglyDisapprove: 0.4,
          somewhatDisapprove: 0.4,
          neutral: 11.9,
          somewhatApprove: 32.1,
          stronglyApprove: 55.2
        },
        {
          category: "more than 4000 RMB",
          stronglyDisapprove: 0.0,
          somewhatDisapprove: 0.9,
          neutral: 8.8,
          somewhatApprove: 30.9,
          stronglyApprove: 59.4
        }
      ];
    },
    changeToLocation: function() {
      changeToCategory("changeToLocation", "Location");
      chart.data = [
        {
          category: "rural",
          stronglyDisapprove: 1.2,
          somewhatDisapprove: 1.1,
          neutral: 30.1,
          somewhatApprove: 31.4,
          stronglyApprove: 36.2
        },
        {
          category: "city",
          stronglyDisapprove: 0.5,
          somewhatDisapprove: 0.7,
          neutral: 16.4,
          somewhatApprove: 31.1,
          stronglyApprove: 51.4
        }
      ];
    },
    changeToRegion: function() {
      changeToCategory("changeToRegion", "Region");
      chart.data = [
        {
          category: "west",
          stronglyDisapprove: 0,
          somewhatDisapprove: 1.2,
          neutral: 17.1,
          somewhatApprove: 34.6,
          stronglyApprove: 47.1
        },
        {
          category: "central",
          stronglyDisapprove: 0.7,
          somewhatDisapprove: 0.8,
          neutral: 19.9,
          somewhatApprove: 28.9,
          stronglyApprove: 49.7
        },
        {
          category: "east",
          stronglyDisapprove: 0.8,
          somewhatDisapprove: 0.5,
          neutral: 18.1,
          somewhatApprove: 31.4,
          stronglyApprove: 49.1
        }
      ];
    }
  },
  mounted() {
    chart = am4core.create(this.$refs.chartdiv, am4charts.XYChart);
    chart.hiddenState.properties.opacity = 0; // this creates initial fade-in

    chart.data = [
      {
        category: "14-30 years",
        stronglyDisapprove: 6.8,
        somewhatDisapprove: 7.2,
        neutral: 19.9,
        somewhatApprove: 33.6,
        stronglyApprove: 45.1
      },
      {
        category: "31-50 years",
        stronglyDisapprove: 0.5,
        somewhatDisapprove: 0.5,
        neutral: 17.0,
        somewhatApprove: 28.5,
        stronglyApprove: 53.4
      },
      {
        category: "51-65 years",
        stronglyDisapprove: 0,
        somewhatDisapprove: 4.3,
        neutral: 18.4,
        somewhatApprove: 21.0,
        stronglyApprove: 56.4
      }
    ];

    chart.colors.step = 1;
    chart.padding(30, 30, 10, 30);
    chart.legend = new am4charts.Legend();
    chart.legend.position = "right";
    chart.legend.width = am4core.percent(60);
    chart.legend.labels.template.text = "[white]{name}[/]";
    chart.legend.itemContainers.template.togglable = false;
    chart.legend.reverseOrder = true;

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
