<template>
    <div class="col-xs-12 col-sm-6">
        <p>Server Details are currently not updated</p>
        <p v-if="!serverlists">Please select a server</p>
        <p v-else> Server #{{ serverlists.id}} {{ serverlists.status }}</p>
        <hr>
        <button @click="resetStatus">Change Status to Normal</button>
    </div>

</template>

<script>
import { serverBus } from '../../../main.js'
export default {
    data: () => ({
        serverlists: null
    }),
    methods: {
        resetStatus() {
            this.serverlists.status = 'Normal'
        }
    },
    created() {
        serverBus.$on('serverSelected', (serverlists) => {
            this.serverlists = serverlists
        })
    }
}
</script>

<style>

</style>
