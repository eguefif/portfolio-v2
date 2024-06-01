<script setup>
import ProjectComponent from '@/components/ProjectComponent.vue'
const projects = [
  {
    title: 'Mini Raytracer',
    img: 'https://github.com/PelletierM/miniRT/raw/master/scenes/renders/spheres.png?raw=true',
    description:
      'Mini raytracer coded in c able to render scene with textures and different material.',
    techno: ['c', 'raytracing', 'threading']
  },
  {
    title: 'Mini Raytracer',
    img: 'https://github.com/PelletierM/miniRT/raw/master/scenes/renders/spheres.png?raw=true',
    description:
      'Mini raytracer coded in c able to render scene with textures and different material.',
    techno: ['c', 'raytracing', 'threading']
  },

  {
    title: 'Mini Raytracer',
    img: 'https://github.com/PelletierM/miniRT/raw/master/scenes/renders/spheres.png?raw=true',
    description:
      'Mini raytracer coded in c able to render scene with textures and different material.',
    techno: ['c', 'raytracing', 'threading']
  }
]
</script>

<template>
  <div class="project-box">
    <div class="project-rows">
      <ProjectComponent :project="projects[0]" />
      <ProjectComponent :project="projects[1]" />
    </div>
    <div class="project-rows">
      <ProjectComponent :project="projects[1]" />
    </div>
  </div>
</template>

<style scoped>
.project-box {
  width: 700px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.project-rows {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
}
</style>
