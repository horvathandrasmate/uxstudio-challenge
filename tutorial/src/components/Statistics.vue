<template>
  <div class="relative">
    <div id="statistics-container" class="absolute left">
      <div id="statistics-container-title">Statistics overview</div>
      <div id="statistics-content">
        <table>
          <tr class="statistics-header">
            <td class="selected-stat stat-selector">
              Weekly
              <hr class="stat-header-weekly-hr" />
            </td>
            <td class="stat-selector">
              Monthly
              <hr class="stat-header-monthly-hr" />
            </td>
          </tr>
        </table>
        <hr class="stat-header-hr" />
        <div id="choose-campaign-dropdown">
          <div class="inline dropdown-campaign-title">Choose campaign:</div>
          <div id="dropdown-campaign" class="inline">
            <p id="dropdown-campaign-p" class="inline">All</p>
            <img :src="downArrowSVG" class="dropdown-campaign-arrow" />
          </div>
        </div>
        <svg class="graph" aria-labelledby="title" role="img">
          <title id="title">A line chart showing some information</title>

          <g class="labels x-labels">
            <text x="45" y="155" fill="#8D8D8D" font-weight="bold">MON</text>
            <text x="85" y="155" fill="#8D8D8D" font-weight="bold">TUE</text>
            <text x="125" y="155" fill="#8D8D8D" font-weight="bold">WED</text>
            <text x="165" y="155" fill="#8D8D8D" font-weight="bold">THU</text>
            <text x="205" y="155" fill="#8D8D8D" font-weight="bold">FRI</text>
            <text x="245" y="155" fill="#8D8D8D" font-weight="bold">SAT</text>
            <text x="285" y="155" fill="#8D8D8D" font-weight="bold">SUN</text>
          </g>
          <g class="labels y-labels">
            <text x="10" y="127" fill="#8D8D8D" font-size="9px" text-anchor="start">0</text>
            <text x="10" y="102" fill="#8D8D8D" font-size="9px" text-anchor="start">25</text>
            <text x="10" y="77" fill="#8D8D8D" font-size="9px" text-anchor="start">50</text>
            <text x="10" y="52" fill="#8D8D8D" font-size="9px" text-anchor="start">75</text>
            <text x="10" y="27" fill="#8D8D8D" font-size="9px" text-anchor="start">100</text>
          </g>
          <g class="grid x-grid">
            <line x1="30" x2="285" y1="125" y2="125" />
            <line x1="30" x2="285" y1="100" y2="100" />
            <line x1="30" x2="285" y1="75" y2="75" />
            <line x1="30" x2="285" y1="50" y2="50" />
            <line x1="30" x2="285" y1="25" y2="25" />
          </g>
          <polyline
            fill="none"
            stroke="#F60051"
            stroke-width="2"
            points="
                 45,125
       85,100
       125,117.5
       165,67.5
       205,100
       245,25
       285,75

       
            "
          />
        </svg>
        <table>
          <tr>
            <td class="statistics-data">
              <div class="statistics-data-div selected selected-statistics-data-div stat-top">
                <div class="campaign-stat-number">123</div>
                <div class="campaign-stat-text">
                  <img :src="instagramWhiteSVG" class="inline campaign-stat-svg" />
                  <div class="inline">REACH</div>
                </div>
              </div>
            </td>
            <td class="statistics-data">
              <div class="statistics-data-div stat-top">
                <div class="campaign-stat-number">5 789</div>
                <div class="campaign-stat-text">
                  <img :src="instagramGreySVG" class="inline campaign-stat-svg" />
                  <div class="inline">REACH</div>
                </div>
              </div>
            </td>
          </tr>
          <tr>
            <td class="statistics-data">
              <div class="statistics-data-div">
                <div class="campaign-stat-number">34 567</div>
                <div class="campaign-stat-text">
                  <img :src="instagramGreySVG" class="inline campaign-stat-svg" />
                  <div class="inline">REACH</div>
                </div>
              </div>
            </td>
            <td class="statistics-data">
              <div class="statistics-data-div">
                <div class="campaign-stat-number">5 789</div>
                <div class="campaign-stat-text">
                  <img :src="instagramGreySVG" class="inline campaign-stat-svg" />
                  <div class="inline">REACH</div>
                </div>
              </div>
            </td>
          </tr>
        </table>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",

  data() {
    return {
      snapchatGreySVG: require("../assets/svg/snapchat-grey.svg"),
      instagramGreySVG: require("../assets/svg/instagram-grey.svg"),
      downArrowSVG: require("../assets/svg/arrow-down.svg"),
      instagramWhiteSVG: require("../assets/svg/instagram-white.svg")
    };
  }
};
</script>

<style>
@media screen and (min-width: 1065px) {
  #statistics-content {
    width: 100%;
    background-color: #ffffff;
    padding: 10px;
    padding-top: 0;
    border-radius: 3px;
    box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.09);

    /* padding-right: 0; */
  }
  .statistics-header td {
    width: 50%;
    text-align: center;
  }
  #dropdown-campaign {
    border: solid 1px #d9d9d9;
    border-radius: 3px;
    color: #484848;
    font-size: 12px;
    padding: 5px;
    margin-left: 10px;
  }

  .statistics-data {
    text-align: center;
  }
  .selected .campaign-stat-number {
    color: #ffffff;
    vertical-align: middle;
  }
  .selected .campaign-stat-text {
    color: #ffffff;
    vertical-align: middle;
  }
  .selected {
    background-color: #f60051;
    box-shadow: inset 0px 1px1px #950031;
  }
  #dropdown-campaign-p {
    margin-bottom: 0;
    padding-left: 5px;
    padding-right: 120px;
  }
  .dropdown-campaign-arrow {
    fill: #950031;
  }
  .graph .labels.x-labels {
    text-anchor: middle;
  }
  .statistics-data-div {
    border: solid 1px #d9d9d9;
    border-radius: 3px;
    max-width: 136px;
    height: 60px;
    padding-top: 10px;
    padding-bottom: 10px;
  }
  .selected-statistics-data-div {
    border: 0;
    border-radius: 3px;
    max-width: 136px;
    height: 60px;
    padding-top: 10px;
    -webkit-box-shadow: inset -9px 12px 7px -15px rgba(0, 0, 0, 0.63);
    -moz-box-shadow: inset -9px 12px 7px -15px rgba(0, 0, 0, 0.63);
    box-shadow: inset -9px 12px 7px -15px rgba(0, 0, 0, 0.63);
  }
  .dropdown-campaign-title {
    font-size: 14px;
    padding-left: 10px;
  }
  .graph .labels.y-labels {
    text-anchor: end;
  }
  .stat-top {
    margin-bottom: 20px;
  }
  .campaign-stat-svg {
    padding-bottom: 3px;
    padding-right: 3px;
  }
  .graph {
    height: 170px;
    width: 100%;
  }

  .graph .grid {
    stroke: #ccc;
    stroke-dasharray: 0;
    stroke-width: 1;
  }

  .labels {
    font-size: 13px;
  }
  .chart {
    stroke: #f60051;
    stroke-width: 1;
  }
  .day-lable {
    color: #8d8d8d;
  }
  .label-title {
    font-weight: bold;
    text-transform: uppercase;
    font-size: 12px;
    fill: black;
  }

  .data {
    fill: red;
    stroke-width: 1;
  }
  #statistics-container-title {
    color: #484848;
    font-size: 16px;
    font-weight: 300;
    line-height: 18px;
  }

  #statistics-container {
    /* width: calc(50% - 2vmin); */
    max-width: 325px;
    margin: 0 2vmin 0 2vmin;
    border-radius: 3px;
    /* padding: 10px; */
  }
  #statistics-container-title {
    margin-bottom: 1vmin;
  }
  .stat-selector {
    padding: 10px;
    padding-bottom: 0px;
  }
  .stat-header-hr {
    margin-top: 0;
    margin-bottom: 10px;
  }
  .stat-header-weekly-hr {
    margin-top: 10px;
    margin-bottom: 0;
    color: #f60051;
    background-color: #f60051;
    width: 70px;
    height: 2px;
  }
  .stat-header-monthly-hr {
    margin-top: 10px;
    margin-bottom: 0;
    color: #f60051;
    background-color: #f60051;
    visibility: hidden;
    height: 2px;
    width: 70px;
  }
}
@media screen and (max-width: 1065px) {
  #statistics-content {
    width: 97vmin;
    background-color: #ffffff;
    padding: 10px;
    padding-top: 0;
    border-radius: 3px;
    box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.09);

    /* padding-right: 0; */
  }
  .statistics-header td {
    width: 50%;
    text-align: center;
  }
  #dropdown-campaign {
    border: solid 1px #d9d9d9;
    border-radius: 3px;
    color: #484848;
    font-size: 12px;
    padding: 5px;
    margin-left: 10px;
  }

  .statistics-data {
    text-align: center;
  }
  .selected .campaign-stat-number {
    color: #ffffff;
    vertical-align: middle;
  }
  .selected .campaign-stat-text {
    color: #ffffff;
    vertical-align: middle;
  }
  .selected {
    background-color: #f60051;
    box-shadow: inset 0px 1px1px #950031;
  }
  #dropdown-campaign-p {
    margin-bottom: 0;
    padding-left: 5px;
    padding-right: 120px;
  }
  .dropdown-campaign-arrow {
    fill: #950031;
  }
  .graph .labels.x-labels {
    text-anchor: middle;
  }
  .statistics-data-div {
    border: solid 1px #d9d9d9;
    border-radius: 3px;
    /* max-width: 136px; */
    width: 100%;
    height: 60px;
    padding-top: 10px;
    padding-bottom: 10px;
  }
  .selected-statistics-data-div {
    border: 0;
    border-radius: 3px;
    /* max-width: 136px; */
    width: 100%;
    height: 60px;
    padding-top: 10px;
    -webkit-box-shadow: inset -9px 12px 7px -15px rgba(0, 0, 0, 0.63);
    -moz-box-shadow: inset -9px 12px 7px -15px rgba(0, 0, 0, 0.63);
    box-shadow: inset -9px 12px 7px -15px rgba(0, 0, 0, 0.63);
  }
  .dropdown-campaign-title {
    font-size: 14px;
    padding-left: 10px;
  }
  .graph .labels.y-labels {
    text-anchor: end;
  }
  .stat-top {
    margin-bottom: 20px;
  }
  .campaign-stat-svg {
    padding-bottom: 3px;
    padding-right: 3px;
  }
  .graph {
    height: 170px;
    width: 100%;
  }

  .graph .grid {
    stroke: #ccc;
    stroke-dasharray: 0;
    stroke-width: 1;
  }

  .labels {
    font-size: 13px;
  }
  .chart {
    stroke: #f60051;
    stroke-width: 1;
  }
  .day-lable {
    color: #8d8d8d;
  }
  .label-title {
    font-weight: bold;
    text-transform: uppercase;
    font-size: 12px;
    fill: black;
  }

  .data {
    fill: red;
    stroke-width: 1;
  }
  #statistics-container-title {
    color: #484848;
    font-size: 16px;
    font-weight: 300;
    line-height: 18px;
  }

  #statistics-container {
    /* width: calc(50% - 2vmin); */
    /* max-width: 325px; */
    width: 100%;
    margin: 0 2vmin 0 2vmin;
    border-radius: 3px;
    /* padding: 10px; */
  }
  #statistics-container-title {
    margin-bottom: 1vmin;
  }
  .stat-selector {
    padding: 10px;
    padding-bottom: 0px;
  }
  .stat-header-hr {
    margin-top: 0;
    margin-bottom: 10px;
  }
  .stat-header-weekly-hr {
    margin-top: 10px;
    margin-bottom: 0;
    color: #f60051;
    background-color: #f60051;
    width: 70px;
    height: 2px;
  }
  .stat-header-monthly-hr {
    margin-top: 10px;
    margin-bottom: 0;
    color: #f60051;
    background-color: #f60051;
    visibility: hidden;
    height: 2px;
    width: 70px;
  }
}
</style>
