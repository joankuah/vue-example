<template>
  <div id="app">
    <h1>Tutorial</h1>
    <exercise1/>
  </div>
</template>

<script>
import Exercise1 from './components/Exercise1.vue'

export default {
  name: 'App',
  components: {
    Exercise1
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
