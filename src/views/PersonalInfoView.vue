<template>
  <div class="flex-container">
    <img class="bio-picture" src="@/assets/emmanuel-picture.jpeg" />
    <div class="bio-card">
      <h2 class="bio-text-title">Let me introduce myself</h2>
      <div class="bio-text">
        Lifelong learner, I made my first program when I was sixteen. It was a GCD calculator
        implementing an algorithm I had learned at school. In the first part of my adult life, I
        studied sociology and then became a teacher to share my passion for learning and nurture my
        student's curiosity. After meeting one of my student's father, I realized that talking about
        computers made me feel very good, and I decided to turn what was a passion into a
        profession. I now work as a full stack developper and learn everything I can about
        architecture.
      </div>
    </div>
  </div>
</template>

<style scoped>
.flex-container {
  display: flex;
  flex-direction: row;
  align-items: center;
  width: 40%;
  padding: 15px;
}
@media screen and (max-width: 80rem) {
  .flex-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 40%;
    padding: 15px;
  }
}

.bio-picture {
  width: 300px;
  height: 300px;
  border-radius: 50%;
  object-fit: cover;
  padding: 15px;
  align-items: center;
  justify-content: center;
}

.bio-card {
  padding: 15px;
}

.bio-text {
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.4;
  font-size: 18px;
  text-align: justify;
}
.bio-text-title {
  text-align: center;
}
</style>
