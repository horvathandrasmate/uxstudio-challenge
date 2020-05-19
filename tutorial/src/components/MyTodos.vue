<template>
  <div id="my-to-dos-container">
    <div id="my-to-dos-title">
      My to do's (3)
    </div>
    <div id="my-to-dos-content" class="relative">
      <div id="my-to-dos-scrollbar-holder" class="absolute right">
        <div class="relative">
          <div id="my-to-dos-scrollbar" class="absolute"></div>
        </div>
      </div>
      <div id="posts">
      <div class="top-margin">
      </div>
        <div id="my-to-dos-post-1" class="post">
          <div class="my-to-dos-header">
            <div class="inline-p my-to-dos-names">Ellaria Dorne</div>
            <div class="inline-p">
              uploaded instagram content for proof to your campaign
              <b>'Nike Sneaker Campaign II'</b>
            </div>
          </div>
          <div class="post-data">
            <table>
              <tr>
                <td>
                  <div class="my-to-dos-image">
                    <img :src="todos1SVG" />
                  </div>
                </td>
                <td>
                  <img :src="instagramGreySVG" class="inline" />
                  <div class="inline to-dos-date">
                    02.07.1016
                  </div>
                  <div class="post-text">
                    Who sasy you can't be elegant in sneakers?! :)
                    <div class="inline-p hashtags">
                      #nike #sneakers #morningoutfit #liveyourlife #fashion
                      #dailyfashion #fashionista
                    </div>
                  </div>
                </td>
              </tr>
            </table>

            <table class="post-buttons">
              <tr>
                <td>
                  <button class="add-to-favourites-btn">ACCEPT</button>
                </td>
                <td>
                  <button class="add-to-favourites-btn">DECLINE</button>
                </td>
              </tr>
            </table>
          </div>
        </div>
        <div id="my-to-dos-post-2" class="post">
          <div class="my-to-dos-header">
            <div class="inline-p my-to-dos-names">Amy Champeon</div>
            <div class="inline-p">
              just applied to your open campaign
              <b>'Tennis clothing for men'</b>
            </div>
          </div>
          <div class="post-data">
            <table>
              <tr>
                <td>
                  <div class="my-to-dos-image">
                    <img :src="todos2SVG" />
                  </div>
                </td>
                <td>
                  Amy Champeon
                  <table>
                    <tr>
                      <td class="to-dos-number">34 567</td>
                      <td class="to-dos-number">3 567</td>
                    </tr>
                    <tr>
                      <td class="to-dos-data-label">INSTAGRAM</td>
                      <td class="to-dos-data-label">SNAPCHAT</td>
                    </tr>
                    <tr>
                      <td class="to-dos-data-label">FOLLOWERS</td>
                      <td class="to-dos-data-label">FOLLOWERS</td>
                    </tr>
                  </table>
                </td>
              </tr>
            </table>

            <table class="post-buttons">
              <tr>
                <td>
                  <button class="add-to-favourites-btn">ACCEPT</button>
                </td>
                <td>
                  <button class="add-to-favourites-btn">DECLINE</button>
                </td>
              </tr>
            </table>
          </div>
        </div>
        <div id="my-to-dos-post-3" class="post">
          <div class="my-to-dos-header">
            <div class="inline-p my-to-dos-names">Mike Jones</div>
            <div class="inline-p">
              published content to instagram for campign
              <b>'#DOYOUYOGA'</b>
            </div>
          </div>
          <div class="post-data">
            <table>
              <tr>
                <td>
                  <div class="my-to-dos-image">
                    <img :src="todos3SVG" />
                  </div>
                </td>
                <td>
                  <img :src="instagramGreySVG" class="inline" />
                  <div class="inline to-dos-date">
                    02.07.1016
                  </div>
                  <div class="post-text">
                    My new yoga pants from Nike has arrived, I adore it!
                    <div class="inline-p hashtags">
                      #nike #yoga #sun #namaste #liveyourlife #fashion
                      #dailyfashion #sport #sporty #nature
                    </div>
                  </div>
                </td>
              </tr>
            </table>

            <table class="post-buttons">
              <tr>
                <td>
                  <button class="add-to-favourites-btn">ACCEPT</button>
                </td>
                <td>
                  <button class="add-to-favourites-btn">DECLINE</button>
                </td>
              </tr>
            </table>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "App",

  data() {
    return {
      instagramGreySVG: require("../assets/svg/instagram-grey.svg"),

      todos1SVG: require("../assets/svg/todos-1.svg"),
      todos2SVG: require("../assets/svg/todos-2.svg"),
      todos3SVG: require("../assets/svg/todos-3.svg"),
    };
  },
};
</script>
<style>
#my-to-dos-content {
  background-color: #d8d8d8;
  height: 700px;
  width: 100%;
  border-radius: 3px;
}
#my-to-dos-title {
  color: #484848;
  font-size: 16px;
  font-weight: 300;
  line-height: 18px;
  margin-bottom: 10px;
}
#my-to-dos-scrollbar-holder {
  width: 20px;
  height: 700px;
  background-color: #c6c6c6;
  border-top-right-radius:3px;
}
#my-to-dos-scrollbar {
  height: 120px;
  width: 10px;
  background-color: #a6a6a6;
  border-radius: 13px;
  right: 25%;
  left: 25%;
  top: 10px;
}
.my-to-dos-content {
  width: calc(100%-20px);
  background-color: white;
}

.my-to-dos-names {
  color: #f60051;
}
.hashtags {
  color: #c6c6c6;
}
.post-text {
  color: #484848;
  font-size: 10px;
  font-weight: 400;
  line-height: 12px;
}
.post-data {
  background-color: #ffffff;
}
#posts {
  width: calc(100% - 20px);
  height:700px;
  overflow:hidden;
  
}
.top-margin{
    height:1.5vmin;
}.my-to-dos-image{
    margin:1vmin 1vmin 1vmin 1vmin;
}
.my-to-dos-header {
  background-color: #f4f4f4;
  font-size: 12px;
  font-weight: 400;
  line-height: 14px;
  padding: 1.5vmin 2vmin 1.5vmin 1.5vmin;
}
.to-dos-date {
  color: #c6c6c6;
  font-size: 9px;
  font-weight: 400;
  line-height: 11px;
}
.to-dos-number {
  color: #f60051;
  font-size: 14px;
  font-weight: 700;
  line-height: 17px;
}
#my-to-dos-container {
  height: 750px;
  overflow: hidden;
  position: absolute;
  right: 0;
  top: 0;
  margin: 0 -5vmin 0 2vmin;
  width: calc(40% - 4vmin);
  margin-left: 300px;

}
.to-dos-data-label {
  color: #c6c6c6;
  font-size: 8px;
  font-weight: 700;
  line-height: 10px;
}
.post {
  width: calc(100% - 20px - 1vmin);
  margin: 0.5vmin auto;
  margin-top: 1vmin;
  border-radius: 3px;
  border: 1px solid #FFFFFF;
}
.post-buttons td {
  text-align: center;
  width:50%;
}
.post-buttons td button{
    background-color:#FFFFFF;
    width:80%;
    margin: 2vmin 0 1vmin 0;
}
.post-buttons{
    border-top: 1px solid #d9d9d9;
     
}
</style> 
