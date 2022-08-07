<template>
  <div class="user">
    <!-- <p>Component User</p> -->
    <h3>{{ user.email }}</h3>
    <button v-on:click="handleDelete" class="delete">Delete</button>
  </div>
</template>

<script>
export default {
  name: "user",
  props: {
    user: {
      type: Object,
      default: null,
    },
  },
  data() {
    return {};
  },
  methods: {
    handleDelete() {
      let data = {
        id: this.user.id
      }
      this.$emit('deleteUser', data)
    }
  }
};
</script>

<style>
.user {
  position: relative;
}
.user .delete {
  position: absolute;
  top: 0;
  right: 0;
}
</style>