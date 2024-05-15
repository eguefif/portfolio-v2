<script setup>
import NavItem from '@/components/NavItem.vue'
import { onMounted, ref } from 'vue'
import ProjectsService from '@/services/ProjectsService.js'

const projects = ref(null)
onMounted(() => {
  ProjectsService.getProjects()
    .then((response) => {
      projects.value = response.data
    })
    .catch((error) => {
      console.log(error)
    })
})
</script>

<template>
  <div class="nav">
    <RouterLink class="nav-item" :to="{ name: 'home' }">About me</RouterLink>
    <NavItem class="nav-item" v-for="project in projects" :key="project.id" :project="project" />
  </div>
  <RouterView />
</template>

<style scoped>
.nav-item {
  font-size: 18px;
  padding: 8px;
  text-decoration: none;
}
.nav {
  display: flex;
  flex-direction: row;
  justify-content: center;
}
</style>
