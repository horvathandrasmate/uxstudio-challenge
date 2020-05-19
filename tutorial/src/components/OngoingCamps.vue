<template>
  <div id="ongoing-camps">
    <div id="ongoing-camps-title">
      <p class="ongoing-campaign-title-p">Ongoing Campaigns</p>
    </div>
    <div id="active-campaign-1" class="campaign">
      <table>
        <tr>
          <td class="relative">
            <img :src="ongoingCampaigns1SVG" class="ongoing-camps-pic inline" />
            <img :src="ringbellSVG" class="absolute" id="ringbell-svg" />
            <div class="absolute" id="used-platforms">
              <img :src="instagramRedSVG" class="used-platforms-icon" />
              <img :src="snapchatRedSVG" class="used-platforms-icon" />
              <img />
            </div>
          </td>
          <td>
            <div class="campaign-mid-text inline">
              <div class="active-text inline">ACTIVE</div>
              <div class="closes-in-x-days inline">
                <p class="closes-in-x-days-p">Closes in 3 days</p>
              </div>
              <div class="x-influencers">9 INFLUENCERS</div>
              <div class="ongoing-campaign-title">NIKE Sneaker Campaign Summer II</div>
            </div>
          </td>
          <td>
            <table class="campaign-stats">
              <tr>
                <td>
                  <div class="campaign-stat-number">12 567</div>
                  <div class="campaign-stat-text">
                    <img :src="instagramGreySVG" class="inline campaign-stat-icon" />
                    <div class="inline">REACH</div>
                  </div>
                </td>
                <td>
                  <div class="campaign-stat-number">1 789</div>
                  <div class="campaign-stat-text">
                    <img :src="instagramGreySVG" class="inline campaign-stat-icon" />
                    <div class="inline">LIKES</div>
                  </div>
                </td>
                <td>
                  <div class="campaign-stat-number">876</div>
                  <div class="campaign-stat-text">
                    <img :src="instagramGreySVG" class="inline campaign-stat-icon" />
                    <div class="inline">COMMENTS</div>
                  </div>
                </td>
              </tr>
              <tr>
                <td>
                  <div class="campaign-stat-number">10 782</div>
                  <div class="campaign-stat-text">
                    <img :src="snapchatGreySVG" class="inline campaign-stat-icon" />
                    <div class="inline">OPENS</div>
                  </div>
                </td>
                <td>
                  <div class="campaign-stat-number">789</div>
                  <div class="campaign-stat-text">
                    <img :src="snapchatGreySVG" class="inline campaign-stat-icon" />
                    <div class="inline">SCREENS</div>
                  </div>
                </td>
                <td>
                  <div class="campaign-stat-number">67%</div>
                  <div class="campaign-stat-text">
                    <img :src="snapchatGreySVG" class="inline campaign-stat-icon" />
                    <div class="inline">COMPLETION</div>
                  </div>
                </td>
              </tr>
            </table>
          </td>
        </tr>
      </table>
    </div>
    <div id="active-campaign-2" class="campaign">
      <table>
        <tr>
          <td class="relative">
            <img :src="ongoingCampaigns2SVG" class="ongoing-camps-pic inline" />
            <div class="absolute" id="used-platforms">
              <img :src="instagramRedSVG" class="used-platforms-icon"/>
            </div>
          </td>
          <td>
            <div class="campaign-mid-text inline">
              <div class="active-text inline">ACTIVE</div>
              <div class="closes-in-x-days inline">
                <p class="closes-in-x-days-p">Closes in 8 days</p>
              </div>
              <div class="x-influencers">11 INFLUENCERS</div>
              <div class="ongoing-campaign-title">#DOYOUYOGA Campaign</div>
            </div>
          </td>
          <td>
            <table class="campaign-stats">
              <tr>
                <td>
                  <div class="campaign-stat-number">34 567</div>
                  <div class="campaign-stat-text">
                    <img :src="instagramGreySVG" class="inline campaign-stat-icon" />
                    <div class="inline">REACH</div>
                  </div>
                </td>
                <td>
                  <div class="campaign-stat-number">5 789</div>
                  <div class="campaign-stat-text">
                    <img :src="instagramGreySVG" class="inline campaign-stat-icon" />
                    <div class="inline">LIKES</div>
                  </div>
                </td>
                <td>
                  <div class="campaign-stat-number">234</div>
                  <div class="campaign-stat-text">
                    <img :src="instagramGreySVG" class="inline campaign-stat-icon" />
                    <div class="inline">COMMENTS</div>
                  </div>
                </td>
              </tr>
            </table>
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
      ongoingCampaigns1SVG: require("../assets/svg/ongoing-campaigns-1.svg"),
      ongoingCampaigns2SVG: require("../assets/svg/ongoing-campaigns-2.svg"),
      snapchatGreySVG: require("../assets/svg/snapchat-grey.svg"),
      instagramGreySVG: require("../assets/svg/instagram-grey.svg"),
      snapchatRedSVG: require("../assets/svg/snapchat-red.svg"),
      instagramRedSVG: require("../assets/svg/instagram-red.svg"),
      ringbellSVG: require("../assets/svg/ringbell.svg")
    };
  }
};
</script>
<style>
#new-campaign-button {
  border: solid 1px #e6004c;
  background: #f60051;
  width: 167.41px;
  height: 16px;
  color: #ffffff;
  font-size: 13px;
  font-weight: 700;
  line-height: 16px;
  width: 185px;
  height: 34px;
  border-radius: 3px;
}
#dashboard-title {
  width: 145.64px;
  height: 22px;
  color: #484848;
  font-size: 18px;
  font-weight: 700;
  line-height: 22px;
}
#ongoing-camps-title {
  width: 137.28px;
  height: 18px;
  color: #484848;
  font-size: 16px;
  font-weight: 300;
  line-height: 18px;
}
.campaign {
  width: 619.9px;
  height: 114px;
  background: #ffffff;
  box-shadow: 0px 2px4px rgba(0, 0, 0, 0.09);
  border-radius: 3px;
}
.ongoing-camps-pic {
  position: relative;
  top: 0;
}
.active-text {
  color: #8d8d8d;
  font-size: 10.3px;
  font-weight: 700;
  line-height: 13px;
  text-align: center;
  width: 51px;
  height: 14px;
  border: solid 1px #d9d9d9;
  border-radius: 2px;
}
.closes-in-x-days {
  width: 68.72px;
  height: 12px;
  color: #8d8d8d;
  font-size: 10px;
  font-weight: 400;
  line-height: 12px;
  margin-left: 10px;
  /* padding-bottom: 50px; */
}
.x-influencers {
  height: 14px;
  color: #f60051;
  font-size: 12px;
  font-weight: 700;
  line-height: 14px;
}
.ongoing-campaign-title {
  width: 213px;
  height: 36px;
  color: #484848;
  font-size: 16px;
  font-weight: 300;
  line-height: 18px;
}
.campaign-mid-text {
  position: relative;
}
.campaign-stats {
  margin-right: 60px;
}
.campaign-stat-number {
  color: #f60051;
  font-size: 18px;
  font-weight: 700;
  line-height: 22px;
  text-align: center;
}
.campaign-stat-text {
  color: #8d8d8d;
  font-size: 8px;
  font-weight: 700;
  line-height: 10px;
  text-align: center;
  margin-bottom: 5px;
  margin-top: 2px;
}

#ringbell-svg {
  top: 20px;
  left: 81px;
}
#used-platforms {
  background: #ffffff;
  width: auto;
  height: auto;
  bottom: 10px;
  left: 0;
  padding-left: 4px;
  /* max-width: 52px; */
  max-height: 24px;
}
.campaign {
  margin: 1vmin 2vmin 2vmin 0;
  width: 100%;
  padding-right: 30px;
}
#ongoing-camps {
  margin-left: 2vmin;
  width: calc(60% + 4vmin);

  margin-right: 2vmin;
}

.campaign-mid-text {
  margin-left: 18px;
}
/* #used-platforms img {
  margin-left: 1vmin;
} */
.ongoing-campaign-title-p {
  white-space: nowrap;
}
.closes-in-x-days-p {
  white-space: nowrap;
  font-size: 12px;
}
.campaign-stat-icon {
  padding-right: 5px;
  padding-bottom: 2px;
}
.used-platforms-icon {
  height: 13px;
  margin-bottom: 4px;
  margin-right: 5px;
  margin-left: 3px;
}
</style>
