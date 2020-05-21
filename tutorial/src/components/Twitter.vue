<template>
  <div id="app">
    <pre id="json"></pre>
  </div>
</template>

<script>
var Twitter = require('twitter');

var client = new Twitter({
  consumer_key: 'fiJI62jvuYSfQyOP3Ww9zQNcc',
  consumer_secret: 'gqu25quBzuSmEAOrrGJFZqDwb65STvQbc7AR9bEskla20eyivY',
  access_token_key: '789512009851211777-I1WatKTzTSKA8uZjY2trAg1vQmtPypj',
  access_token_secret: 'ouh5iG4na38flswkaeb3vd3LnVxfWjxWMb2bK8ESy46za'
});

client.post('statuses/update', {status: 'I Love Twitter'},  function(error, tweet, response) {
  if(error) throw error;
  console.log(tweet);  // Tweet body.
  console.log(response);  // Raw response object.
});
</script>
<style></style>
