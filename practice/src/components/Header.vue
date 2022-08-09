<template>
  <header>
    <h1>{{ title }}</h1>
    <Button
      :text="showAddTask ? 'Close': 'Add Task'"
      :color="showAddTask ? 'red' : 'green'"
      @toggle-add-task="$emit('toggle-add-task')"
    />
  </header>
</template>

<script>
import Button from "./Button.vue";
export default {
  name: "Header",
  props: {
    title: {
      type: String,
      default: "Header Hello to the world",
    },
    showAddTask: Boolean,
  },
  components: {
    Button,
  },
  methods: {
  }
};
</script>

<style>
header {
  display: flex;
  justify-content: space-betwwen;
  align-items: center;
  margin-bottom: 20px;
}
</style>