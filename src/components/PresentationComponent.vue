<script setup>
import { ref } from 'vue'

const name = ref('Emmanuel Guefif')
const description = ref(
  "Lifelong learner, I made my first program when I was sixteen. It was a GCD calculator implementing an algorithm I had learned at school. I soon made my first website for my parent's music association using PHP/SPIP and HTML/CSS. When I moved to a big city to study, I realized how complex the world was and I wanted to understand it. So, I studied sociology and then became a teacher to share my passion for learning and nurture my student's curiosity. I’ve never given up on programming. In the meantime, I studied a bit of Java and C++. More recently, I fell into the AI and Python rabbit hole. After meeting one of my student's father, I realized that talking about computers made me feel very good, and I decided to turn what was a passion into a profession. I am now about to finish the 42 common core and am eager to start as a programmer."
)
const pictureUrl = ref('http://localhost:5173/src/assets/emmanuel-picture.jpeg')
</script>

<template>
  <div class="main-container">
    <div class="box">
      <div class="row">
        <img :src="pictureUrl" />
        <div class="column">
          <h1>{{ name }}</h1>
          <p>{{ description }}</p>
        </div>
      </div>
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

.row {
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
