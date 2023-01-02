<template>
    <div>
      <no-ssr>
        <apexchart
          height="250"
          type="bar"
          :options="options"
          :series="series"
        ></apexchart>
      </no-ssr>
    </div>
  </template>
  <script>
  if (process.client) {
    var VueApexCharts = require("vue-apexcharts");
  }
  export default {
    components: { apexchart: VueApexCharts },
    data: function () {
      return {
        options: {
          chart: {
            id: "vuechart-example",
          },
          xaxis: {
            categories: ['FST','FSE','FD','FSSA','FLASH','ENS','ENSP','ENSAF','ISG','ENAM','ISEPS'],
          },
        },
        series: [
          {
            name: "series-1",
            data: [77, 40, 45, 50, 49, 60, 70, 85,80,75,98],
          },
        ],
      };
    },
  };
  </script>
  <style></style>
  