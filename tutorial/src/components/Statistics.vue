<template>
  <div class="relative">
    <div id="statistics-container" class="absolute left">
      <div id="statistics-container-title">
        Statistics overview
      </div>
      <div id="statistics-content">
        <table>
          <tr class="statistics-header">
            <td class="selected-stat">
              Weekly
            </td>
            <td>
              Monthly
            </td>
          </tr>
        </table>

        <div id="choose-campaign-dropdown">
          <div class="inline">
            Choose campaign
          </div>
          <div id="dropdown-campaign" class="inline">
            All
            <img :src="downArrowSVG" class="" />
          </div>
        </div>
        <svg class="graph" aria-labelledby="title" role="img">
          <title id="title">A line chart showing some information</title>

          <g class="labels x-labels">
            <text x="45" y="155">MON</text>
            <text x="85" y="155">TUE</text>
            <text x="125" y="155">WED</text>
            <text x="165" y="155">THU</text>
            <text x="205" y="155">FRI</text>
            <text x="245" y="155">SAT</text>
            <text x="285" y="155">SUN</text>
          </g>
          <g class="labels y-labels">
            <text x="25" y="125">0</text>
            <text x="25" y="100">25</text>
            <text x="25" y="75">50</text>
            <text x="25" y="50">75</text>
            <text x="25" y="25">100</text>
          </g>
          <g class="grid x-grid">
            <line x1="30" x2="285" y1="125" y2="125"></line>
            <line x1="30" x2="285" y1="100" y2="100"></line>
            <line x1="30" x2="285" y1="75" y2="75"></line>
            <line x1="30" x2="285" y1="50" y2="50"></line>
            <line x1="30" x2="285" y1="25" y2="25"></line>
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
            <td class="selected statistics-data">
              <div class="campaign-stat-number">123</div>
              <div class="campaign-stat-text">
                <img :src="instagramWhiteSVG" class="inline" />
                <div class="inline">
                  REACH
                </div>
              </div>
            </td>
            <td class=" statistics-data">
              <div class="campaign-stat-number">5 789</div>
              <div class="campaign-stat-text">
                <img :src="instagramGreySVG" class="inline" />
                <div class="inline">
                  REACH
                </div>
              </div>
            </td>
          </tr>
          <tr>
            <td class=" statistics-data">
              <div class="campaign-stat-number">34 567</div>
              <div class="campaign-stat-text">
                <img :src="instagramGreySVG" class="inline" />
                <div class="inline">
                  REACH
                </div>
              </div>
            </td>
            <td class=" statistics-data">
              <div class="campaign-stat-number">5 789</div>
              <div class="campaign-stat-text">
                <img :src="instagramGreySVG" class="inline" />
                <div class="inline">
                  REACH
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
      downArrowSVG: require("../assets/svg/down-arrow.svg"),
      instagramWhiteSVG: require("../assets/svg/instagram-white.svg"),
    };
  },
};
</script>

<style>
#statistics-content {
  width: 100%;
  background-color: #ffffff;
}
.statistics-header td {
  width: 50%;
  text-align: center;
}
#dropdown-campaign {
  border: solid 1px #d9d9d9;
}

.statistics-data {
  border: solid 1px #d9d9d9;
  border-radius: 3px;
}
.selected .campaign-stat-number {
  color: #ffffff;
}
.selected .campaign-stat-text {
  color: #ffffff;
}
.selected {
  background-color: #f60051;
  box-shadow: inset 0px 1px1px #950031;
}

.graph .labels.x-labels {
  text-anchor: middle;
}

.graph .labels.y-labels {
  text-anchor: end;
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
  width: calc(50% - 4vmin);
  margin: 0 2vmin 0 2vmin;
  border-radius: 3px;
}
#statistics-container-title {
  margin-bottom: 1vmin;
}
</style>
