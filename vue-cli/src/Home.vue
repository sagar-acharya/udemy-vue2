<template>
    <div>
        <span>Global Component</span>
        <h1>Server Status {{ status }}</h1>
        <hr>
        <button @click="changeStatus">Change Status</button>
        <hr>
        <span>Local Component</span>
        <hr>
        <server-status v-for="server in 5"></server-status>
    </div>
</template>

<script>
    import ServerStatus from './ServerStatus.vue';
    export default {
        data: function() {
            return {
                status: 'Critical'
            }
        },
        methods: {
            changeStatus(){
                this.status = 'Normal';
            }
        },
        components: {
            'server-status': ServerStatus
        }
    }
</script>