<template>
    <li class="list-group-item" style="cursor: pointer" @click="changeStatus">
        Server #{{ server.id }} :: Status - {{ server.name }}
    </li>
</template>

<script>
    import { Bus } from '../../main';
    export default {
        props: ['server'],
        methods: {
            changeStatus: function() {
                Bus.$emit('serverSelected',this.server);
            }
        }
    }
</script>

<style>

</style>
