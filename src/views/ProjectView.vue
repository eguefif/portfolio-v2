<script setup>
import { ref } from 'vue'
const props = defineProps({
  id: { required: true }
})
const projects = ref([
  {
    title: 'Web Development Project',
    id: '0',
    description:
      "Embark on a web development journey by creating your own personal portfolio website. This project involves learning HTML, CSS, and JavaScript to design and build a responsive site that showcases your skills, projects, and experiences. Incorporate interactive elements like a contact form and dynamic project gallery to enhance user engagement. By completing this project, you'll gain a solid understanding of front-end development and a tangible showcase of your capabilities."
  },
  {
    title: 'IoT Smart Home System',
    id: '1',
    description:
      'Dive into the Internet of Things (IoT) with a smart home automation project. Utilize microcontrollers like Arduino or Raspberry Pi to connect and control various household devices such as lights, thermostats, and security cameras. Develop a mobile app or web interface to manage these devices remotely. This project will teach you about hardware programming, wireless communication, and user interface design, providing a comprehensive introduction to IoT technologies.'
  },
  {
    title: 'Machine Learning Model',
    id: '2',
    description:
      "Explore the world of artificial intelligence by developing a machine learning model. Choose a dataset, such as image recognition or natural language processing, and use Python libraries like TensorFlow or Scikit-Learn to build and train your model. Experiment with different algorithms and parameters to optimize performance. Through this project, you'll gain practical experience in data preprocessing, model training, and evaluation, essential skills for any aspiring data scientist."
  }
])
const project = ref(projects.value.find((item) => item.id == props.id))
//const project = ref(projects.value[0])
</script>

<template>
  <div class="main-container">
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
