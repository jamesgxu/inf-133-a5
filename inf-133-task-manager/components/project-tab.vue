<template>
    <div class="project-tab">
      <h2>{{ project.name }}</h2>
      <button @click="createNewTask">+ Add Task</button>
      <div class="columns">
        <div v-for="status in statuses" :key="status" class="column">
          <h3>{{ status }}</h3>
          <TaskContainer :status="status" />
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import TaskContainer from './TaskContainer.vue';
  import { useRoute } from 'vue-router';
  
  const statuses = ['Backlog', 'Doing', 'Review', 'Done'];
  const project = ref({ name: 'CS101 Project', id: 1 }); // You can replace this with dynamic data later
  
  const createNewTask = () => {
    console.log('New task creation logic here');
  };
  </script>
  
  <style scoped>
  .project-tab {
    padding: 20px;
  }
  .columns {
    display: flex;
    gap: 20px;
  }
  .column {
    border: 1px solid #ccc;
    padding: 10px;
    width: 200px;
    flex: 1;
  }
  </style>
  
