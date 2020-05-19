<template> 
<div></div>
</template>
<script>
import axios from "axios";

let config = {
  headers: {
    oauth_consumer_key: "gqu25quBzuSmEAOrrGJFZqDwb65STvQbc7AR9bEskla20eyivY",
  },
};
let data = {
  HTTP_CONTENT_LANGUAGE: self.language,
};

axios
  .post(
    "https://api.twitter.com/1.1/search/tweets.json?q=from%3Atwitterdev&result_type=mixed&count=2",
    data,
    config
  )
  .then(response => {
    console.log(response);
  });
</script>
<style></style>
