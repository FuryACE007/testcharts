<template>
  <div id="app">
    <Creatinine></Creatinine>
    <Weight></Weight>
    <BPstolic></BPstolic>
    <BPdiastolic></BPdiastolic>
    <HBvsPharma></HBvsPharma>
  </div>
</template>

<script>
import Creatinine from './components/Creatinine-chart.vue'
import Weight from './components/Weight-chart.vue'
import BPstolic from './components/BPstolic-chart.vue'
import BPdiastolic from './components/BPdiastolic-chart.vue'
import HBvsPharma from './components/HBvsPharma-chart.vue'

export default {
  name: 'App',
  components: {
    Creatinine,
    Weight,
    BPstolic,
    BPdiastolic,
    HBvsPharma,
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
