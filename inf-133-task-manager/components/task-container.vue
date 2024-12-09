<template>
    <div class="task-container">
      <TaskItem v-for="task in tasks" :key="task.id" :task="task" />
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import TaskItem from './TaskItem.vue';
  
  const tasks = ref([
    { id: 1, name: 'Task 1', dueDate: '2024-12-10', status: 'Backlog' },
    { id: 2, name: 'Task 2', dueDate: '2024-12-12', status: 'Doing' },
  ]);
  </script>
  
  <style scoped>
  .task-container {
    margin-top: 20px;
  }
  </style>
  
