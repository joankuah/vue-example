<template>
    <div>
        <h1>Exercise 2</h1>
        <!-- 1) Show an alert when the Button gets clicked -->
        <div>
            <button v-on:click="showAlert">Show Alert</button>
        </div>
        <hr>
        <!-- 2) Listen to the "keydown" event and store the value in a data 
        property (hint: event.target.value gives you the value) -->
        <div>
            <input type="text" v-on:keydown="value = $event.target.value">
            <p>{{ value }}</p>
        </div>
        <hr>
        <!-- 3) Adjust the example from 2) to only fire if the "keydown" is the ENTER key -->
        <div>
            <input type="text" v-on:keydown.enter="value = $event.target.value">
            <p>{{ value }}</p>
        </div>
    </div>
</template>

<script>
export default {
    data: () => ({
        value: ''
    }),
    methods: {
        showAlert: function() {
            alert("You have clicked the button !")
        }
    }
}
</script>