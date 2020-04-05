<template>
  <div>
    <h1>Exercise 1</h1>
    <p>VueJS is pretty cool - {{ name }} ({{ age }})</p>
    <hr>
    <p>My age mulitipled by 3 is {{ ageMultipled() }}</p>
    <hr>
    <p>RANDOM NUMBR BETWEEN 0 AND 100: {{ randomNumber(0,100) }}</p>
    <hr>
    <div>
      <img :src="imageLink">
    </div>
    <hr>
    <div>
      <input type="text" :value="name">
    </div>

  </div>
</template>

<script>
export default {
  data: () => ({
    name: 'Joan',
    age: 20,
    imageLink : 'https://techcrunch.com/wp-content/uploads/2015/10/screen-shot-2015-10-08-at-4-20-16-pm.png?w=730&crop=1'
  }),
  methods: {
    ageMultipled() {
      return this.age*3
    },
    randomNumber(min, max) {
      return Math.floor(Math.random(min, max) * Math.floor(max))
    }
  }
}
</script>
