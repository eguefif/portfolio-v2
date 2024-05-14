<script setup>
import { ref } from 'vue'

const name = ref('Emmanuel Guefif')
const description = ref('Here a short presentation of myself')
const pictureUrl = ref('https://www.eguefif.org/media/media/1700661299735_UBi9tmJ.jpeg')
</script>

<template>
  <div class="flex-container">
    <h1>{{ name }}</h1>
    <p>{{ description }}</p>
    <img :src="pictureUrl" />
  </div>
</template>

<style scoped>
h1 {
  font-size: 20px;
}
</style>
