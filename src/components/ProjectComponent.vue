<script setup>
import { computed } from 'vue'
const props = defineProps(['project'])

const imgSrc = computed(() => {
  return new URL(props.project.img, import.meta.url).href
})
</script>
<template>
  <div class="project-card">
    <div class="flip-card-inner">
      <div class="card-front">
        <h1>{{ props.project.title }}</h1>
        <img :src="imgSrc" />
      </div>
      <div class="card-back">
        <p>{{ props.project.description }}</p>
        <ul>
          <li class="techno" v-for="item in props.project.techno" :key="item">{{ item }}</li>
        </ul>
        <a class="github-logo" :href="props.project.github" target="_blank"
          ><img src="@/assets/github.png"
        /></a>
      </div>
    </div>
  </div>
</template>

<style scoped>
.project-card {
  background-color: transparent;
  width: 300px;
  height: 200px;
  perspective: 1000px;
  margin: 10px;
}
.flip-card-inner {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.8s;
  transform-style: preserve-3d;
}
.project-card:hover .flip-card-inner {
  transform: rotateY(180deg);
}
.card-front,
.card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
}

.card-front {
  background-color: #fff;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  text-align: center;
}
.card-back {
  background-color: #f0f0f0;
  transform: rotateY(180deg);
  color: black;
  border-radius: 10px;
}
.project-card img {
  width: 100%;
  height: auto;
  border-bottom: 1px solid #ddd;
}
.project-card h1 {
  font-size: 24px;
  margin: 15px 0;
  color: #333;
}
.github-logo img {
  width: 30px;
  height: 30px;
  display: inline-block;
  transition: transform 0.2s;
}
.github-logo img:hover {
  transform: scale(1.2);
}
.techno {
  text-align: left;
}
</style>
