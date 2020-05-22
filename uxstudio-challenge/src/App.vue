<template>
  <App />
</template>

<script>

import Vue from 'vue'
import App from './App'

console.log('[i] Starting client app')

Vue.config.productionTip = false

new Vue({
  render: h => h(App),
  components: { App }
}).$mount('#app')
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
