<template>
  <div class="task-list">
    <ul :key="task.id" v-for="task in tasks">
        <li>{{ task.text }}</li>
    </ul>
  </div>
</template>

<script>
export default {
    name: 'Tasks',
    props: {
        tasks: Array,
    }
}
</script>

<style>

</style>e