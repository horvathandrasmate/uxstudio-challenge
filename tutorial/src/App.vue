<template>
  <div id="app">
   <Twitter /> 
  </div>
</template>

<script>
//import Navbar from "./components/Navbar.vue";
//import Dashboard from "./components/Dashboard.vue";
import Twitter from "./components/Twitter.vue";

export default {
  name: "App",
  components: {
  //  Navbar,
  //  Dashboard,
    Twitter
  },
};
</script>

<style>
html,
body {
  margin: 0;
  padding: 0;
  background-color: #eae9eb;
  font-family: Lato, sans-serif;
}
</style>
