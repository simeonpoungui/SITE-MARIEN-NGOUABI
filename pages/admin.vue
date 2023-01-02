<template>
    <div>
      <div class="is-flex">
        <div>
          <sidebar />
        </div>
        <div class="topbar">
          <Topbar />
        </div>
      </div>
      <div>
        <div class="chart">
          <chart />
        </div>
      </div>
      <div
        class="is-flex is-flex-direction-row is-justify-content-space-between b-chart"
      >
        <div>
          <p class="forme">
            Graphe states établissements de formation <br />
            professionnelle
          </p>
          <Tab_etab />
        </div>
        <div class="chart2">
          <div class="is-flex is-justify-content-space-between">
            <div class="box i" type="is-info">
              <p class="text-align">
                Effectif Université Marien Ngouabi en general
                <span class="color">100%</span>
              </p>
              <br />
              <i class="mdi icn mdi-cupcake"></i>
            </div>
            <div class="box if" type="is-success">
              <p class="text-align">
                Effectif établissements de formation professionnelle
                <span class="color">80%</span>
              </p>
              <br /><i class="mdi icn mdi-deviantart"></i>
            </div>
          </div>
          <div class="">
            <div class="is-flex block hvr-shutter-out-vertical">
              <div class="blc">
                <a class="link-item" href="/"
                  ><i class="mdi icon-admin mdi-network"></i
                ></a>
              </div>
              <div class="blc">
                <a class="link-item" href="/"
                  ><i class="mdi icon-admin mdi-view-grid-outline"></i
                ></a>
              </div>
              <div class="blc">
                <a class="link-item" href="/"
                  ><i class="mdi icon-admin mdi-view-day"></i
                ></a>
              </div>
              <div class="blc">
                <a class="link-item" href="/"
                  ><i class="mdi icon-admin mdi-transcribe"></i
                ></a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  import Chart from "../components/chart.vue";
  import Chart2 from "../components/chart2.vue";
  import sidebar from "../layouts/sidebar.vue";
  import Topbar from "../layouts/topbar.vue";
  import Tab_etab from "../components/tab_etab.vue";
  export default {
    components: { sidebar, Topbar, Chart, Chart2, Tab_etab },
  };
  </script>
  
  <style>
  .topbar {
    width: 100%;
  }
  .state {
    margin-left: 200px;
    border: 1px solid black;
    width: 100%;
    height: 90vh;
  }
  .chart {
    height: 40px;
    margin-left: 210px;
  }
  .b-chart {
    width: 100%;
    height: 350px;
    margin-top: 200px;
    margin-left: 205px;
    padding-right: 230px;
  }
  .chart2 {
    width: 50%;
    padding-top: 30px;
  }
  .icn {
    font-size: 50px;
    margin-left: 80px;
    margin-top: -20px;
  }
  .forme {
    padding-top: 22px;
    font-weight: bold;
    text-align: center;
  }
  .i {
    width: 250px;
    height: 200px;
    padding-top: 10px;
  }
  .if {
    width: 250px;
    height: 200px;
    padding-top: 10px;
    margin-left: 70px;
  }
  .text-align {
    text-align: center;
  }
  .block {
    width: 100%;
    height: 85px;
    border-radius: 10px;
    padding: 20px;
  }
  .link-item {
    color: white;
  }
  .link-item:hover {
    color: white;
  }
  .color {
    color: #0f4c5c;
    font-weight: bold;
    font-size: 30px;
  }
  .icon-admin {
    font-size: 40px;
  }
  .blc {
    margin-left: 71px;
    margin-top: -8px;
  }
  </style>
  