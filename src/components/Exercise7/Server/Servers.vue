<template>
    <div class="col-xs-12 col-sm-6">
        <ul class="list-group">
            <server-lists v-for="server in servers" :key="server" :serverlists="server"/>
        </ul>
    </div>
</template>

<script>
import ServerLists from './ServerLists.vue'

export default {
    components: {
        ServerLists
    },
    data: () => ({
        servers: [
            {
                id: 1,
                status:'Normal'
            },
            {
                id: 2,
                status: 'Critical'
            },
            {
                id: 3,
                status: 'Unknown'
            },
            {
                id: 4,
                status: 'Normal'
            }
        ]
    })
}
</script>

<style>

</style>
