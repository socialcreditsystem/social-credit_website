<template>
  <div class="map">
    <div id="chartdiv">
    </div>
  </div>
</template>

<script>
import * as am4core from "@amcharts/amcharts4/core";
import am4themes_animated from "@amcharts/amcharts4/themes/animated";
import am4geodata_chinaLow from "@amcharts/amcharts4-geodata/chinaLow";
import * as am4maps from "@amcharts/amcharts4/maps";

export default {
  name: "ChinaMap",
  mounted() {
    am4core.useTheme(am4themes_animated);

    var chart = am4core.create("chartdiv", am4maps.MapChart);

    var latlong = {
      example1: { latitude: 24, longitude: 116 },
      example2: { latitude: 28, longitude: 117 },
      example3: { latitude: 32, longitude: 120 }
    };

    var mapData = [
      {
        id: "example1",
        name: "Beispiel 1",
        value: 382392
      },
      {
        id: "example2",
        name: "Beispiel 2",
        value: 382392
      },
      {
        id: "example3",
        name: "Beispiel 3",
        value: 382392
      }
    ];

    // Add lat/long information to data
    for (var i = 0; i < mapData.length; i++) {
      mapData[i].latitude = latlong[mapData[i].id].latitude;
      mapData[i].longitude = latlong[mapData[i].id].longitude;
    }

    // Set map definition
    chart.geodata = am4geodata_chinaLow;

    // Set projection
    chart.projection = new am4maps.projections.Miller();

    // Create map polygon series
    var polygonSeries = chart.series.push(new am4maps.MapPolygonSeries());
    //polygonSeries.include = ["CN"];
    polygonSeries.useGeodata = true;

    // Configure series
    var polygonTemplate = polygonSeries.mapPolygons.template;
    polygonTemplate.tooltipText = "{name}[bold]{socialCreditSince}[/]";
    polygonTemplate.fill = am4core.color("#CCCCCC");

    // Create hover state and set alternative fill color
    var hs = polygonTemplate.states.create("hover");
    hs.properties.fill = am4core.color("#AAAAAA");

    // Remove Antarctica
    polygonSeries.exclude = ["AQ"];

    // Add some data of states which should be highlighted
    polygonSeries.data = [
      {
        id: "CN-QH",
        name: "Qinghai",
        socialCreditSince: ": Social Credit-System seit 2018",
        fill: am4core.color("#5fcc9e")
      },
      {
        id: "CN-GZ",
        name: "Guizhou",
        socialCreditSince: ": Social Credit-System seit 2014",
        fill: am4core.color("#5fcc9e")
      }
    ];

    // Bind "fill" property to "fill" key in data
    polygonTemplate.propertyFields.fill = "fill";

    var imageSeries = chart.series.push(new am4maps.MapImageSeries());
    imageSeries.data = mapData;
    imageSeries.dataFields.value = "value";

    var imageTemplate = imageSeries.mapImages.template;
    imageTemplate.propertyFields.latitude = "latitude";
    imageTemplate.propertyFields.longitude = "longitude";
    imageTemplate.nonScaling = true;

    var circle = imageTemplate.createChild(am4core.Circle);
    circle.fillOpacity = 1;
    circle.fill = "#5fcc9e";
    circle.tooltipText = "{name}: [bold]{value}[/]";
    circle.radius = 10;
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.map {
  padding: 40px 0;
}
#chartdiv {
  width: 70%;
  height: 500px;
  margin: 0 auto;
}
</style>
