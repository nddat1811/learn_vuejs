<template>
  <div class="user">
    <!-- <p>Component User</p> -->
    <h3>{{ user.email }}</h3>
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
};
</script>

<style>
</style>