<script setup>
import PersonalInfoView from '@/views/PersonalInfoView.vue'
import ProjectsView from '@/views/ProjectsView.vue'
</script>

<template>
  <div class="main-box">
    <div class="overlay"></div>
    <div class="layout">
      <div class="title">
        <h1>I am Emmanuel Guefif</h1>
        <h2>Junior full stack developer</h2>
        <a class="resume" target="_blank" href="/files/resume.pdf" download>Get my resume</a>
      </div>
      <div class="portfolio">
        <PersonalInfoView />
        <div class="vl"></div>
        <ProjectsView />
      </div>
      <div class="footer">
        <a class="logo-social" href="https://www.github.com/eguefif" target="_blank"
          ><img src="@/assets/github-white.png"
        /></a>
        <a class="logo-social" href="https://www.linkedin.com/in/eguefif" target="_blank"
          ><img src="@/assets/in-white.png"
        /></a>
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
  font-family: Arial, Helvetica, sans-serif;
}
@media screen and (max-width: 80rem) {
  body {
    height: 100%;
    margin: 0;
    padding: 0;
    font-family: Arial, Helvetica, sans-serif;
    overflow: scroll;
  }
}
.title {
  text-align: center;
  width: 100%;
  color: white;
  z-index: 3;
  margin-top: 50px;
}
h1 {
  font-size: 45px;
  color: white;
}
h2 {
  font-size: 25px;
  color: white;
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
.portfolio-normal {
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
@media screen and (max-width: 80rem) {
  .portfolio {
    display: flex;
    flex-direction: column;
    z-index: 2;
    position: relative;
    align-items: center;
    justify-content: center;
    color: white;
    height: 100%;
    width: 100%;
  }
}

.vl {
  height: 250px;
  width: 2px;
  margin: 30px;
  background-color: white;
}
@media screen and (max-width: 80rem) {
  .vl {
    height: 2px;
    width: 250px;
    margin: 30px;
    background-color: white;
  }
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
@media screen and (max-width: 80rem) {
  .main-box {
    background: #151515 url(./assets/nebula.jpg) no-repeat center center;
    background-size: cover;
    background-attachment: fixed;
    position: relative;
    z-index: 0;
    margin: 0;
    padding: 0;
    width: 100%;
    height: 100%;
  }
  .overlay {
    z-index: 1;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
    margin: 0;
    padding: 0;
  }
}
.resume {
  text-decoration: none;
  color: white;
  border: 1px solid white;
  padding: 10px;
  margin: 15px !important;
}
.logo-social img {
  width: 50px;
  height: 50px;
  display: inline-block;
  margin: 15px;
  transition: transform 0.2s;
}
.logo-social img:hover {
  transform: scale(1.2);
}
.footer {
  display: flex;
  z-index: 4;
  justify-content: center;
  margin-bottom: 25px;
}
</style>
