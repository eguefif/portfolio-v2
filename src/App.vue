<script setup>
import PersonalInfoView from '@/views/PersonalInfoView.vue'
import ProjectsView from '@/views/ProjectsView.vue'
</script>

<template>
  <div class="main-box">
    <div class="overlay"></div>
    <div class="layout">
      <div class="title">I am Emmanuel Guefif</div>
      <div class="portfolio">
        <PersonalInfoView />
        <div class="vl"></div>
        <ProjectsView />
      </div>
    </div>
  </div>
</template>

<style>
html,
body {
  height: 100%;
  margin: 0;
  padding: 0;
}
.title {
  text-align: center;
  width: 100%;
  font-size: 45px;
  position: relative;
  color: white;
  z-index: 3;
  margin-top: 50px;
}
.layout {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100%;
  position: relative;
}
.portfolio {
  display: flex;
  flex-direction: row;
  z-index: 2;
  position: relative;
  align-items: center;
  justify-content: center;
  color: white;
  height: 100%;
  width: 100%;
}
.vl {
  height: 250px;
  width: 2px;
  margin: 30px;
  background-color: white;
}
.main-box {
  background: #151515 url(./assets/nebula.jpg) no-repeat center center;
  background-size: cover;
  background-attachment: fixed;
  position: fixed;
  z-index: 0;
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
}
.overlay {
  z-index: 1;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  margin: 0;
  padding: 0;
}
</style>
