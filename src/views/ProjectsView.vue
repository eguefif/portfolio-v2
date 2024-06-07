<script setup>
import ProjectComponent from '@/components/ProjectComponent.vue'
const projects = [
  {
    title: 'Weather app',
    img: 'weatherapp.png',
    description: 'Weather app fething data and displaying current, hourly and week weather',
    techno: ['dart/flutter', 'api request', 'threading'],
    github: 'https://www.github.com/eguefif/weatherapp'
  },
  {
    title: 'Mini Raytracer',
    img: 'spheres.png',
    description:
      'Mini raytracer coded in c able to render scenes with textures and different materials.',
    techno: ['c', 'raytracing', 'threading'],
    github: 'www.github.com/eguefif/miniRT'
  },

  {
    title: 'ft_transcendence',
    img: 'transcendence.png',
    description: 'Pong platform SPA website with a custom server side pong.',
    techno: ['django', 'javascript', 'python (asyncio, websocket)', 'docker'],
    github: 'https://www.github.com/eguefif/ft_transcendence'
  },
  {
    title: 'ft_irc',
    img: 'irc.png',
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
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  width: 50%;
  gap: 20px;
}

@media screen and (max-width: 80rem) {
  .project-box {
    column-count: 1;
    align-items: center;
    justify-content: center;
  }
}
</style>
