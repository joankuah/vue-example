<template>
    <div>
        <li
            class="list-group-item"
            @click="populateDetails"
        >
            Server #{{ serverlists.id }}
        </li>
    </div>
</template>

<script>
import { serverBus } from '../../../main.js'

export default {
    props: {
        serverlists: {
            type: Array,
            required: true
        }
    },
    methods: {
        populateDetails() {
            serverBus.$emit('serverSelected', this.serverlists)
        }
    }
}
</script>