<template>
  <div id="dashboard" class="relative">
    <div id="page-title">
      <div id="dashboard-title" class="inline">
        MY DASHBOARD
      </div>
      <button id="new-campaign-button" class="inline">
        CREATE A NEW CAMPAIGN
      </button>
    </div>
    <div class="relative">
      <OngoingCamps />
      <div id="lower-panel">
        <Statistics />
        <TopInfluencers />
      </div>
      <MyTodos />
      <Twitter />
    </div>
  </div>
</template>

<script>
import OngoingCamps from "./OngoingCamps.vue";
import Statistics from "./Statistics.vue";
import TopInfluencers from "./TopInfluencers.vue";
import MyTodos from "./MyTodos.vue";
// import Twitter from "./Twitter.vue";

export default {
  name: "App",
  components: {
    OngoingCamps,
    Statistics,
    TopInfluencers,
    MyTodos,
    // Twitter,
  },
  data() {
    return {};
  },
};
</script>

<style>
.inline {
  display: inline-block;
}
.relative {
  position: relative;
}
.absolute {
  position: absolute;
}
.add-to-favourites-btn {
  color: #f60051;
  font-size: 10px;
  font-weight: 700;
  line-height: 12px;
  text-align: center;
  border-radius: 3px;
  border: solid 1px #d9d9d9;
  width: 85px;
  height: 34px;
}
table {
  width: 100%;
}
.right {
  right: 0;
}
.inline-p {
  display: inline;
}
#dashboard {
  margin-top: 2vmin;
  height: 904px;
  width: 1016px;
}
#dashboard-title {
  margin-left: 2vmin;
  margin-right: 2vmin;
}
#lower-panel {
  width: 60%;
  position: relative;
}
.left {
  left: 0;
}
</style>
