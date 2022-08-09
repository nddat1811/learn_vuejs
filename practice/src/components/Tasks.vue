<template>
  <div class="task-list">
    <ul :key="task.id" v-for="task in tasks">
      <li>
        <Task
          :task="task"
          @delete-task="$emit('deleteTask', task.id)"
          @toggle-reminder="$emit('toggleReminder', task.id)"
        />
      </li>
    </ul>
  </div>
</template>

<script>
import Task from "./Task.vue";
export default {
  name: "Tasks",
  props: {
    tasks: Array,
  },
  components: {
    Task,
  },
  emits: ["deleteTask", "toggleReminder"],
};
</script>

<style>
</style>e