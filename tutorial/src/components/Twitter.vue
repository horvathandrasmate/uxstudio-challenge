<template>
  <div id="data"></div>
</template>
<script>
// inside your .vue file
import Json from "../assets/json/data.json";
var vue = new Vue({
  el: "#dashboard",
  data: {
    variable: "",
  },
  computed: {
    currentDashboard: function() {
      return this.variable;
    },
  },
});
export default {
  data() {
    return {
      variable: Json,
    };
  },
};
console.log(this.variable);
</script>
<style></style>
