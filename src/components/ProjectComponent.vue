<script setup>
const props = defineProps(['project'])
</script>
<template>
  <div class="project-card">
    <div class="flip-card-inner">
      <div class="card-front">
        <h1>{{ props.project.title }}</h1>
        <img :src="props.project.img" />
      </div>
      <div class="card-back">
        <p>fsadfadsfsadf sadf sadf sdaf sdafds fds fds fsd</p>
        <ul>
          <li>language c</li>
          <li>Raytracing math and physics</li>
          <li>team work</li>
        </ul>
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
</style>
