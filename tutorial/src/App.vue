<template>
  <div id="app">
    <Navbar />
    <Dashboard />
    <OngoingCamps />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Dashboard from "./components/Dashboard.vue";
import OngoingCamps from "./components/OngoingCamps.vue";

export default {
  name: "App",
  components: {
    Navbar,
    Dashboard,
    OngoingCamps,
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
