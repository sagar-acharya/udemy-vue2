<template>
    <div class="col-xs-12 col-sm-6">
        <ul class="list-group">
            <app-server v-for="server in servers" :server="server"></app-server>
        </ul>
    </div>
</template>

<script>
    import Server from './Server.vue';
    export default {
        data: function() {
            return {
                servers: [
                    { id: 1, name: 'Normal' },
                    { id: 2, name: 'Critical' },
                    { id: 3, name: 'Unknown' },
                    { id: 4, name: 'Normal' }
                ]
            }
        },
        components: {
            'app-server': Server
        }
    }
</script>

<style>

</style>
