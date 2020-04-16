<template>
    <div class="component">
        <h3>You may edit the User here</h3>
        <p>Edit me!</p>
        <p>User Age: {{ userage }}</p>
        <button @click="editAge">Edit Age</button>
    </div>
</template>

<script>
import { eventBus } from '../main'

export default {
    props: {
        userage: {
            type: Number,
            required: true
        }
    },
    methods: {
        editAge() {
            this.userage = 20
            // this.$emit('ageWasEdited', this.userage)
            // eventBus.$emit('ageWasEdited', this.userage)
            eventBus.changeAge(this.userage)
        }
    }
}
</script>

<style scoped>
    div {
        background-color: lightgreen;
    }
</style>
