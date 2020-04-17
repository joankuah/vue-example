<template>
    <div class="component">
        <h3>You may view the User Details here</h3>
        <p>Many Details</p>
        <!-- I want to output the name in the child component -->
        <p>User Name: {{ username }}</p>
        <p>User Age: {{ userage }}</p>
        <button @click="resetName">Reset Name</button>
        <button @click="resetFunction()">Reset to Default Name</button>
    </div>
</template>

<script>
import { eventBus } from '../main'

export default {
    props: {
        username: {
            type: String,
            required: true
            //when you use required you cant use default
            //it is used to set a default value when props is not passed
            // default: 'Max
            //type: Object,
            //default: function() {
                // return {
                    // name:'Max
                // }
            // }
        },
        userage: {
            type: Number,
            required: true
        },
        resetFunction: Function
    },
    methods: {
        resetName() {
            this.username = 'John'
            this.$emit('nameWasReset', this.username)
        }
    },
    created() {
        eventBus.$on('ageWasEdited', (age)=> {
            this.userage = age
        })
    }
}
</script>

<style scoped>
    div {
        background-color: lightcoral;
    }
</style>
