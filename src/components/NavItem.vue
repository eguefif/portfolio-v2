<script setup>
defineProps({
  project: {
    Object,
    required: true
  }
})
</script>

<template>
  <RouterLink class="nav-item" :to="{ name: 'project', params: { id: project.id } }">
    | {{ project.title }}
  </RouterLink>
</template>

<style scoped>
.nav-item {
  text-decoration: none;
}
</style>
