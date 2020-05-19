<template>
  <div id="top-influencers-container" class="absolute right">
    <div id="top-influencers-title">
      Top Influencers
    </div>
    <div id="influencers-list">
      <table>
        <tr>
          <td class="influencers-picture">
            <img :src="influencer1SVG" />
          </td>
          <td class="influencers-data"></td>
          <div class="influencer-name">
            Mildred Estrada
          </div>
          <div class="engagement-rate">
            Engagement rate: 25%
          </div>
          <td class="influencers-button">
            <div class="add-to-favourites-btn">ADD TO FAVOURITES</div>
          </td>
        </tr>
        <tr>
          <td class="influencers-picture">
            <img :src="influencer2SVG" />
          </td>
          <td class="influencers-data"></td>
          <div class="influencer-name">
            Charlotte Morris
          </div>
          <div class="engagement-rate">
            Engagement rate: 20%
          </div>
          <td class="influencers-button">
            <div class="add-to-favourites-btn">ADD TO FAVOURITES</div>
          </td>
        </tr>
        <tr>
          <td class="influencers-picture">
            <img :src="influencer3SVG" />
          </td>
          <td class="influencers-data"></td>
          <div class="influencer-name">
            Sadie Brooks
          </div>
          <div class="engagement-rate">
            Engagement rate: 18%
          </div>
          <td class="influencers-button">
            <div class="add-to-favourites-btn">ADD TO FAVOURITES</div>
          </td>
        </tr>
        <tr>
          <td class="influencers-picture">
            <img :src="influencer4SVG" />
          </td>
          <td class="influencers-data"></td>
          <div class="influencer-name">
            Mary Nichols
          </div>
          <div class="engagement-rate">
            Engagement rate: 18%
          </div>
          <td class="influencers-button">
            <div class="add-to-favourites-btn">ADD TO FAVOURITES</div>
          </td>
        </tr>
        <tr>
          <td class="influencers-picture">
            <img :src="influencer5SVG" />
          </td>
          <td class="influencers-data"></td>
          <div class="influencer-name">
            Teresa Austin
          </div>
          <div class="engagement-rate">
            Engagement rate: 17%
          </div>
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
      influencer5SVG: require("../assets/svg/influencer-5.svg"),
    };
  },
};
</script>
<style>
#influencers-list {
  background-color: #ffffff;
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
.engagement-rate {
  color: #8d8d8d;
  font-size: 10px;
  font-weight: 400;
  line-height: 12px;
}

#top-influencers-container {
  width: 50%;
  border-radius: 3px;
}
#top-influencers-title {
  margin-bottom: 1vmin;
}
#influencers-list tr {
  border-bottom: 1px solid #d8d8d8;
}
</style>
