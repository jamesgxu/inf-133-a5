<template>
    <div class="home">
      <h1>Project Manager</h1>
      <button @click="createNewProject">+ New Project</button> 
      <div v-for="project in projects" :key="project.id" class="project-card">
        <p>{{ project.name }}</p>
        <router-link :to="`/project/${project.id}`">View Project</router-link>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import { useRouter } from 'vue-router';
  
  const projects = ref([
    { id: 1, name: 'CS101 Project' },
    { id: 2, name: 'CS102 Project' },
  ]);
  
  const createNewProject = () => {
    console.log('New project creation logic here');
  };
  </script>
  
  <style scoped>
  .home {
    text-align: center;
  }
  .project-card {
    margin: 10px;
    padding: 20px;
    border: 1px solid #ccc;
    cursor: pointer;
  }
  </style>
  