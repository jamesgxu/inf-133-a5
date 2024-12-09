<template>
    <div class="task-item">
      <p>{{ task.name }} - Due: {{ task.dueDate }}</p>
    </div>
  </template>
  
  <script setup>
  defineProps({
    task: Object,
  });
  </script>
  
  <style scoped>
  .task-item {
    padding: 10px;
    border: 1px solid #ccc;
    margin-bottom: 10px;
  }
  </style>
  
