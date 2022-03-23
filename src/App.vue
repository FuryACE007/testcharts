<template>
  <div id="app">
    <Creatinine></Creatinine>
    <Weight></Weight>
  </div>
</template>

<script>
import Creatinine from './components/Creatinine-chart.vue'
import Weight from './components/Weight-chart.vue'

export default {
  name: 'App',
  components: {
    Creatinine,
    Weight,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  margin-left: 350px;
  
}
</style>
