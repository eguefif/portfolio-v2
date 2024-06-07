<script setup>
import ProjectComponent from '@/components/ProjectComponent.vue'
const projects = [
  {
    title: 'Weather app',
    img: './src/assets/weatherapp.png',
    description:
      'Mini raytracer coded in c able to render scene with textures and different material.',
    techno: ['dart/flutter', 'api request', 'threading'],
    github: 'https://www.github.com/eguefif/weatherapp'
  },
  {
    title: 'Mini Raytracer',
    img: './src/assets/spheres.png',
    description:
      'Mini raytracer coded in c able to render scene with textures and different material.',
    techno: ['c', 'raytracing', 'threading'],
    github: 'www.github.com/eguefif/miniRT'
  },

  {
    title: 'ft_transcendence',
    img: './src/assets/transcendence.png',
    description: 'Pong platform spa website with a custom server side pong.',
    techno: ['django', 'javascript', 'python (asyncio, websocket)', 'docker'],
    github: 'https://www.github.com/eguefif/ft_transcendence'
  },
  {
    title: 'ft_irc',
    img: './src/assets/irc.png',
    description: 'Basic IRC server that works with WeeChat',
    techno: ['c++', 'polymorphism'],
    github: 'https://www.github.com/eguefif/ft_irc'
  }
]
</script>

<template>
  <div class="project-box">
    <ProjectComponent :project="projects[0]" />
    <ProjectComponent :project="projects[1]" />
    <ProjectComponent :project="projects[2]" />
    <ProjectComponent :project="projects[3]" />
  </div>
</template>

<style scoped>
.project-box {
  column-count: 2;
  align-items: center;
  justify-content: center;
}
@media screen and (max-width: 80rem) {
  .project-box {
    column-count: 1;
    align-items: center;
    justify-content: center;
  }
}
</style>
