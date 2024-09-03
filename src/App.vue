<script setup lang="ts">
import HeroSection from './components/HeroSection.vue'
import HeaderSection from './components/HeaderSection.vue'
import AboutSection from './components/AboutSection.vue'
import ExperienceSection from './components/ExperienceSection.vue'
import { onMounted } from 'vue'


onMounted(() => {
  localStorage.setItem('theme', 'dark');
})
</script>

<template>
  <div>
    <header-section></header-section>
    <div class="min-h-screen flex items-center justify-center bg-blue-900 dark:bg-gray-950">
      <hero-section />
    </div>
    <div class="min-h-screen flex items-center justify-center bg-blue-900 dark:bg-gray-950">
      <about-section />
    </div>
    <div class="min-h-screen flex items-center justify-center bg-blue-900 dark:bg-gray-950">
      <experience-section />
    </div>
  </div>

</template>

<style scoped>

</style>
