<template>
    <div class="col-xs-12 col-sm-6">
        <p v-if="!server">Please select server</p>
        <p v-else="!server">Server #{{server.id}} selected, status {{server.name}}</p>
    </div>

</template>

<script>
    import { Bus } from '../../main';
    export default {
        data: function() {
            return {
                server: null
            }
        },
        created() {
            Bus.$on('serverSelected',(server) => {
                this.server = server;
            });
        }
    }
</script>

<style>

</style>
