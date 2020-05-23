<template>
  <div id="twitter">
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

    rendered += '<tr class="twitter-post-container">';
    rendered += '<td class="twitter-profile-picture">';
    rendered += '<img src="' + status.user.profile_image_url + '" />';
    rendered += "</td>";
    rendered += ' <td class="influencers-data">';
    rendered +=
      '<div class="influencer-name">' +
      status.user.name +
      "   , @" +
      status.user.screen_name +
      "</div>";
    rendered += '<div class="twitter-text-content">' + status.text + "</div>";
    rendered += "</td>";

    rendered += "</tr>";
    let parent = document.getElementById("posts-container");
    parent.insertAdjacentHTML("beforeend", rendered);
  });
}
fetch("https://guamanpj.eu/twitter-api/index.php")
  .then((response) => response.json())
  .then((data) => afterFetch(data));
</script>
<style>
/*.post-container{
  background-color:white;
  border:2px solid black;
  border-radius:3px;
  display:inline-block;
  width:200px;
  text-align:justify;
  
  
}
#twitter{
  box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.09);
  border-radius:3px;
  height:100%; 
  width:805px;
  position:relative;
  display:block;
  z-index:4;
}*/
.twitter-profile-picture img {
  margin: 1.5vmin 2vmin 1.5vmin 2vmin;
  height: 25px;
  width: 25px;
}
.twitter-text-content {
  color: #8d8d8d;
  font-size: 12px;
  font-weight: 400;
  line-height: 12px;
}
#twitter-posts-list {
  width: 100%;
  border-radius: 3px;
  left: 370px;
  top: 0px;
  box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.09);
}
#posts-container{

}
.twitter-post-container {
  background-color: white;
  height:25px;
  border-radius:3px;
  margin:5px 4px 5px 4px;
}
#twitter {
  max-width: 325px;
  border-radius: 3px;
  margin-left:20px;
  margin-bottom:30px;
}
</style>
