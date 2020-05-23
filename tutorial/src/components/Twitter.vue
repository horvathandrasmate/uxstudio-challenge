<template>
  <div id="twitter">
    <p class="twitter-title">Twitter API</p>
    <div id="twitter-posts-list">
      <table id="posts-container"></table>
    </div>
  </div>
</template>
<script>
function afterFetch(data) {
  console.log(data);
  data.statuses.forEach(function(status) {
    let rendered = "";
    rendered += '<tbody class="twitter-post-container">';
    rendered += "<tr>";
    rendered += '<td class="twitter-profile-picture">';
    rendered += '<img src="' + status.user.profile_image_url + '" />';
    rendered += "</td>";
    rendered += ' <td class="twitter-data">';
    rendered +=
      '<div class="twitter-names">' +
      '<p class="twitter-username">' +
      status.user.name +
      "</p>" +
      '<p class="twitter-nice-name">    @' +
      status.user.screen_name +
      "</p></div>";
    rendered += '<div class="twitter-text-content">' + status.text + "</div>";
    rendered += "</td>";

    rendered += "</tr>";
    rendered += "</tbody>";
    let parent = document.getElementById("posts-container");
    parent.insertAdjacentHTML("beforeend", rendered);
  });
}
fetch("https://guamanpj.eu/twitter-api/index.php")
  .then(response => response.json())
  .then(data => afterFetch(data));
</script>
<style>
@media screen and (min-width: 1065px) {
  .twitter-profile-picture img {
    margin: 0vmin 2vmin 1.5vmin 2vmin;
    height: 50px;
    /* width: 25px; */
    border-radius: 50%;
  }
  .twitter-text-content {
    color: #8d8d8d;
    font-size: 18px;
    font-weight: 400;
    line-height: 20px;
    padding-bottom: 15px;
  }
  #twitter-posts-list {
    width: 100%;
    border-radius: 3px;
    left: 370px;
    top: 0px;
    box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.09);
  }
  #posts-container {
  }
  .twitter-post-container {
    background-color: white;
    /* height:25px; */
    border-radius: 3px;
    margin: 5px 4px 5px 4px;
    width: 625px;
    border: 1px lightgray solid;
  }
  #twitter {
    max-width: 625px;
    border-radius: 3px;
    margin-left: 20px;
    margin-bottom: 30px;
  }
  .twitter-username {
    font-size: 18px;
    vertical-align: bottom;
    /* margin-top: 30px; */
    margin-bottom: 0;
    padding-top: 15px;
    color: #f60051;
  }
  .twitter-nice-name {
    font-size: 15px;
    color: #484848;
  }
  hr {
    margin: 0;
    margin-top: 20px;
  }
  .twitter-profile-picture {
    vertical-align: top;
    padding-top: 20px;
  }
  .twitter-title {
    width: 213px;
    /* height: 24px; */
    color: #484848;
    font-size: 16px;
    font-weight: 300;
    line-height: 18px;
    margin-bottom: 10px;
  }
}
@media screen and (max-width: 1065px) {
    .twitter-profile-picture img {
    margin: 0vmin 2vmin 1.5vmin 2vmin;
    height: 50px;
    /* width: 25px; */
    border-radius: 50%;
  }
  .twitter-text-content {
    color: #8d8d8d;
    font-size: 18px;
    font-weight: 400;
    line-height: 20px;
    padding-bottom: 15px;
    padding-right: 15px;
  }
  #twitter-posts-list {
    width: 100%;
    border-radius: 3px;
    left: 370px;
    top: 0px;
    box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.09);
  }
  #posts-container {
  }
  .twitter-post-container {
    background-color: white;
    /* height:25px; */
    border-radius: 3px;
    margin: 5px 4px 5px 4px;
    width: 625px;
    border: 1px lightgray solid;
  }
  #twitter {
    max-width: 97vmin;
    border-radius: 3px;
    margin-left: 2vmin;
    margin-bottom: 30px;
  }
  .twitter-username {
    font-size: 18px;
    vertical-align: bottom;
    /* margin-top: 30px; */
    margin-bottom: 0;
    padding-top: 15px;
    color: #f60051;
  }
  .twitter-nice-name {
    font-size: 15px;
    color: #484848;
  }
  hr {
    margin: 0;
    margin-top: 20px;
  }
  .twitter-profile-picture {
    vertical-align: top;
    padding-top: 20px;
  }
  .twitter-title {
    width: 213px;
    /* height: 24px; */
    color: #484848;
    font-size: 16px;
    font-weight: 300;
    line-height: 18px;
    margin-bottom: 10px;
  }
}
</style>
