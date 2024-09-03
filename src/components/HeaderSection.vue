<template>
  <header class="w-full p-2 md:p-5 flex justify-between items-center bg-inherit fixed top-0 z-50">
    <div class="text-xl font-bold text-gray-100 dark:text-white"></div>
<!--    <nav class="hidden md:flex space-x-6">
      <a href="#home" class="text-gray-100 dark:text-gray-300 hover:text-green-400">Home</a>
      <a href="#about" class="text-gray-100 dark:text-gray-300 hover:text-green-400">About</a>
      <a href="#experience" class="text-gray-100 dark:text-gray-300 hover:text-green-400">Experience</a>
      <a href="#work" class="text-gray-100 dark:text-gray-300 hover:text-green-400">Work</a>
      <a href="#contact" class="text-gray-100 dark:text-gray-300 hover:text-green-400">Contact</a>
    </nav>-->
    <div class="flex items-center space-x-4">
      <button @click="toggleDarkMode" class="p-2 rounded-full bg-gray-200 dark:bg-gray-700">
        <template v-if="isDarkMode">
          <SunIcon  class="w-6 h-6 text-yellow-400"></SunIcon>
        </template>
        <template v-else>
          <MoonIcon class="w-6 h-6 text-gray-900"></MoonIcon>
        </template>
      </button>
      <button @click="isMenuOpen = !isMenuOpen" class="md:hidden p-2 rounded-md bg-gray-200 dark:bg-gray-700">
        <svg v-if="isMenuOpen" class="w-6 h-6 text-gray-800 dark:text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
        </svg>
        <svg v-else class="w-6 h-6 text-gray-800 dark:text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
        </svg>
      </button>
    </div>
<!--    <div v-if="isMenuOpen" class="md:hidden absolute top-16 right-4 w-48 bg-white dark:bg-gray-800 shadow-lg rounded-lg p-4 space-y-4">
      <a href="#home" class="block text-gray-600 dark:text-gray-300 hover:text-green-400">Home</a>
      <a href="#about" class="block text-gray-600 dark:text-gray-300 hover:text-green-400">About</a>
      <a href="#experience" class="block text-gray-600 dark:text-gray-300 hover:text-green-400">Experience</a>
      <a href="#work" class="block text-gray-600 dark:text-gray-300 hover:text-green-400">Work</a>
      <a href="#contact" class="block text-gray-600 dark:text-gray-300 hover:text-green-400">Contact</a>
    </div>-->
  </header>
</template>

<script setup lang="ts">
import { defineComponent, ref, onMounted } from 'vue';
import { SunIcon, MoonIcon } from '@heroicons/vue/24/solid'

const isDarkMode = ref(false);
const isMenuOpen = ref(false);

defineComponent({
  name: 'HeaderSection'
});

const toggleDarkMode = () => {
  isDarkMode.value = !isDarkMode.value;
  if (isDarkMode.value) {
    document.documentElement.classList.add('dark');
    localStorage.setItem('theme', 'dark');
  } else {
    document.documentElement.classList.remove('dark');
    localStorage.setItem('theme', 'light');
  }
}

onMounted(() => {
  const savedTheme = localStorage.getItem('theme');
  if (savedTheme === 'dark') {
    isDarkMode.value = true;
    document.documentElement.classList.add('dark');
  }
});
</script>

<style scoped>
/* Additional styles if needed */
</style>
