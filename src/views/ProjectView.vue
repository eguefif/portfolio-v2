<script setup>
import { ref, onMounted, watchEffect } from 'vue'
import ProjectsService from '@/services/ProjectsService.js'

const props = defineProps({
  id: { required: true }
})

const project = ref(null)

onMounted(() => {
  watchEffect(() => {
    project.value = null
    ProjectsService.getProject(props.id)
      .then((response) => {
        project.value = response.data
      })
      .catch((error) => {
        console.log(error)
      })
  })
})
</script>

<template>
  <div v-if="project" class="main-container">
    <div class="box">
      <h1>{{ project.title }}</h1>
      <p>{{ project.description }}</p>
    </div>
  </div>
</template>

<style scoped>
.main-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

h1 {
  font-size: 25px;
}

img {
  width: 35%;
  height: 35%;
  border-radius: 50%;
  object-fit: cover;
}

p {
  max-width: 500px;
  padding-left: 35px;
  font-family: 'Comic Sans MS', 'Comic Sans';
  font-size: 16px;
  line-height: 1.7;
  float: right;
}

.column {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.box {
  display: flex;
  width: 900px;
  border: solid 2px #dddd;
  padding: 15px;
  align-items: center;
  background-color: #757575;
  border-radius: 2%;
  box-shadow: 10px 15px 10px black;
}
</style>
