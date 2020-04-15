<template>
  <div id="app">
    <!-- <h1>Tutorial</h1> -->
    <!-- <exercise1/> -->
    <!-- <exercise2/> -->
    <!-- <exercise3/> -->
    <!-- <exercise4/> -->
    <!-- <exercise5/> -->
    <h1>Course Project</h1>
    <base-page/>
  </div>
</template>

<script>
// import Exercise1 from './components/Exercise1.vue'
// import Exercise2 from './components/Exercise2.vue'
// import Exercise3 from './components/Exercise3.vue'
// import Exercise4 from './components/Exercise4.vue'
// import Exercise5 from './components/Exercise5.vue'
import BasePage from './components/BasePage.vue'

export default {
  name: 'App',
  components: {
    // Exercise1
    // Exercise2
    // Exercise3
    // Exercise4
    // Exercise5
    BasePage
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
}
</style>
