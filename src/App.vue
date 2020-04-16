<template>
  <div id="container">
    <div class="row">
        <div class="col-xs-12">
            <app-user></app-user>
        </div>
    </div>
      <!-- <exercise6-header/>
    <hr>
    <div class="row">
      <exercise6-list/>
      <exercise6-details/>
    </div>
    <hr>
      <exercise6-footer/> -->
    <!-- <h1>Tutorial</h1> -->
    <!-- <exercise1/> -->
    <!-- <exercise2/> -->
    <!-- <exercise3/> -->
    <!-- <exercise4/> -->
    <!-- <exercise5/> -->
  </div>
</template>

<script>
// import Exercise1 from './components/Exercise1.vue'
// import Exercise2 from './components/Exercise2.vue'
// import Exercise3 from './components/Exercise3.vue'
// import Exercise4 from './components/Exercise4.vue'
// import Exercise5 from './components/Exercise5.vue'
// import Exercise6Header from './components/shared/Exercise6Header.vue'
// import Exercise6List from './components/server/Exercise6List.vue'
// import Exercise6Details from './components/server/Exercise6Details.vue'
// import Exercise6Footer from './components/shared/Exercise6Footer.vue'
import User from './components/User.vue';

export default {
  name: 'App',
  components: {
    // Exercise1,
    // Exercise2,
    // Exercise3
    // Exercise4
    // Exercise5
    // Exercise6Header,
    // Exercise6List,
    // Exercise6Details,
    // Exercise6Footer
    appUser: User
  }
}
</script>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */

div.component {
  border: 1px solid black;
  padding: 30px;
}
</style>
