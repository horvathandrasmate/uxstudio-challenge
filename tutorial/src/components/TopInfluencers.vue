<template>
  <div id="top-influencers-container" class>
    <div id="top-influencers-title">Top Influencers</div>
    <div id="influencers-list">
      <table id="top-influencers-elements">
        <tr>
          <td class="influencers-picture">
            <img :src="influencer1SVG" />
          </td>
          <td class="influencers-data">
            <div class="influencer-name">Mildred Estrada</div>
            <div class="engagement-rate">Engagement rate: 25%</div>
          </td>
          <td class="influencers-button">
            <div class="add-to-favourites-btn">ADD TO FAVOURITES</div>
          </td>
        </tr>
        <tr>
          <td class="influencers-picture">
            <img :src="influencer2SVG" />
          </td>
          <td class="influencers-data">
            <div class="influencer-name">Charlotte Morris</div>
            <div class="engagement-rate">Engagement rate: 20%</div>
          </td>
          <td class="influencers-button">
            <div class="add-to-favourites-btn">ADD TO FAVOURITES</div>
          </td>
        </tr>
        <tr>
          <td class="influencers-picture">
            <img :src="influencer3SVG" />
          </td>
          <td class="influencers-data">
            <div class="influencer-name">Sadie Brooks</div>
            <div class="engagement-rate">Engagement rate: 18%</div>
          </td>
          <td class="influencers-button">
            <div class="add-to-favourites-btn">ADD TO FAVOURITES</div>
          </td>
        </tr>
        <tr>
          <td class="influencers-picture">
            <img :src="influencer4SVG" />
          </td>
          <td class="influencers-data">
            <div class="influencer-name">Mary Nichols</div>
            <div class="engagement-rate">Engagement rate: 18%</div>
          </td>
          <td class="influencers-button">
            <div class="add-to-favourites-btn">ADD TO FAVOURITES</div>
          </td>
        </tr>
        <tr>
          <td class="influencers-picture">
            <img :src="influencer5SVG" />
          </td>
          <td class="influencers-data">
            <div class="influencer-name">Teresa Austin</div>
            <div class="engagement-rate">Engagement rate: 17%</div>
          </td>
          <td class="influencers-button">
            <div class="add-to-favourites-btn">ADD TO FAVOURITES</div>
          </td>
        </tr>
      </table>
    </div>
  </div>
</template>
<script>
export default {
  name: "App",

  data() {
    return {
      influencer1SVG: require("../assets/svg/influencer-1.svg"),
      influencer2SVG: require("../assets/svg/influencer-2.svg"),
      influencer3SVG: require("../assets/svg/influencer-3.svg"),
      influencer4SVG: require("../assets/svg/influencer-4.svg"),
      influencer5SVG: require("../assets/svg/influencer-5.svg")
    };
  }
};
</script>
<style>
@media screen and (min-width: 1065px) {
  #top-influencers-container {
    position: absolute;
    margin-top: 300px;
  }
  #influencers-list {
    background-color: #ffffff;
    border-radius: 3px;
    box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.09);
  }
  #top-influencers-title {
    color: #484848;
    font-size: 16px;
    font-weight: 300;
    line-height: 18px;
  }
  .influencer-name {
    color: #484848;
    font-size: 12px;
    font-weight: 400;
    line-height: 14px;
  }
  #top-influencers-elements {
    width: 300px;
  }
  .engagement-rate {
    color: #8d8d8d;
    font-size: 10px;
    font-weight: 400;
    line-height: 12px;
  }
  .influencers-button div {
    padding: 0.5vmin 0 0 0;
  }
  .influencers-button {
    position: relative;
  }
  #top-influencers-container {
    width: 300px;
    border-radius: 3px;
    left: 370px;
    top: 0px;
  }
  .influencers-picture img {
    margin: 1.5vmin 2vmin 1.5vmin 2vmin;
  }
  #top-influencers-title {
    margin-bottom: 1vmin;
  }
  #influencers-list tr {
    border-bottom: 2px solid #d8d8d8;
    width: 300px;
  }
}

@media screen and (max-width: 1065px) {
  #top-influencers-container {
    margin-top: 480px;
    margin-left: 2vmin;
    width: 100vmin;
  }
  #influencers-list {
    background-color: #ffffff;
    border-radius: 3px;
    box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.09);
  }
  #top-influencers-title {
    color: #484848;
    font-size: 16px;
    font-weight: 300;
    line-height: 18px;
  }
  .influencer-name {
    color: #484848;
    font-size: 3vmin;
    margin-bottom: 10px;
    font-weight: 400;
    line-height: 14px;
  }
  #top-influencers-elements {
    width: 97vmin;
    margin-right: 3vmin;

  }
  .engagement-rate {
    color: #8d8d8d;
    font-size: 2vmin;
    font-weight: 400;
    line-height: 12px;
  }
  .influencers-button div {
    padding: 0.5vmin 0 0 0;
  }
  .influencers-button {
    position: relative;
  }
  #top-influencers-container {
    width: 97vmin;
    border-radius: 3px;
    left: 370px;
    margin-right: 3vmin;
    top: 0px;
  }
  .influencers-picture img {
    margin: 1.5vmin 2vmin 1.5vmin 2vmin;
  }
  #top-influencers-title {
    margin-bottom: 1vmin;
  }
  #influencers-list tr {
    border-bottom: 2px solid #d8d8d8;
    width: 300px;
  }
}
</style>
