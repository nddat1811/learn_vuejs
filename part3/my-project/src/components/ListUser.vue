<template>
  <div class="list-user">
    <user v-for="user in listUser"
        v-bind:key="user.id"
        v-bind:user="user"
        v-on:deleteUser="deleteUser"
    />
  </div>
</template>

<script>

import User from './User.vue'
export default {
    name: 'list-user',
    props: {
        listUser: {
            type: Array,
            default: []
        }
    },
    data() {
        return {
            
        }
    },
    components: {
        User
    },
    methods: {
        deleteUser(data) {
            this.$emit('deleteUserEvent', data)
        }
    },
}
</script>

<style>
    .list-user {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
    }
    .list-user .user {
        padding: 30px;
        margin-bottom: 30px;
        border: 1px solid #333;
        width: calc(33.3333% - 20px);
    }
</style>