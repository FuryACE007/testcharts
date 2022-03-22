<template>
  <div id="app">
    <Creatinine></Creatinine>
  </div>
</template>

<script>
import Creatinine from './components/Creatinine-chart.vue'

export default {
  name: 'App',
  components: {
    Creatinine
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
