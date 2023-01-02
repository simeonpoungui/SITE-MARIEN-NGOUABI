<template>
    <div>
      <no-ssr>
        <apexchart
          type="bar"
          height="280"
          width="470"
          :options="chartOptions"
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
        series: [
          {
            data: [80, 60, 70, 75, 50, 98, 85],
          },
        ],
        chartOptions: {
          chart: {
            type: "bar",
            height: 430,
          },
          plotOptions: {
            bar: {
              horizontal: true,
              dataLabels: {
                position: "top",
              },
            },
          },
          dataLabels: {
            enabled: true,
            offsetX: -6,
            style: {
              fontSize: "12px",
              colors: ["#fff"],
            },
          },
          stroke: {
            show: true,
            width: 1,
            colors: ["#fff"],
          },
          tooltip: {
            shared: true,
            intersect: false,
          },
          xaxis: {
            categories: ["ISG","ENS","ENSP","ENAM", "FSSA" , "ISEPS", "ENSAF" ],
          },
        },
      };
    },
  };
  </script>
  
  <style></style>
  