<template>
  <div class="flex-container">
    <img class="bio-picture" src="@/assets/emmanuel-picture.jpeg" />
    <div class="bio-card">
      <h1>Let me introduce myself</h1>
      <p>
        Lifelong learner, I made my first program when I was sixteen. It was a GCD calculator
        implementing an algorithm I had learned at school. I soon made my first website for my
        parent's music association using PHP/SPIP and HTML/CSS. When I moved to a big city to study,
        I realized how complex the world was and I wanted to understand it. So, I studied sociology
        and then became a teacher to share my passion for learning and nurture my student's
        curiosity. I’ve never given up on programming. In the meantime, I studied a bit of Java and
        C++. More recently, I fell into the AI and Python rabbit hole. After meeting one of my
        student's father, I realized that talking about computers made me feel very good, and I
        decided to turn what was a passion into a profession. I am now about to finish the 42 common
        core and am eager to start as a programmer.
      </p>
    </div>
  </div>
</template>

<style scoped>
.flex-container {
  display: flex;
  flex-direction: row;
  align-items: center;
  width: 700px;
  padding: 15px;
}

.bio-picture {
  width: 200px;
  height: 200px;
  border-radius: 50%;
  object-fit: cover;
  padding: 15px;
  align-items: center;
  justify-content: center;
}

bio-card {
  padding: 15px;
}
</style>
