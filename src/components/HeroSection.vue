<template>
  <section id="hello" class="min-h-screen flex flex-col justify-center items-start p-8 md:p-20">
    <p class="text-green-400 text-sm md:text-lg font-mono mb-2">Hi, my name is</p>
    <h1 class="text-white text-4xl md:text-6xl font-bold mb-4">Kevin Mukhami</h1>
    <h2 class="text-gray-400 text-3xl md:text-5xl font-semibold mb-6">I build things for the web.</h2>
    <p class="text-gray-100 max-w-lg mb-8">
      I'm a software developer specializing in building exceptional digital experiences.
      Currently, I'm focused on building responsive full-stack web applications.
    </p>
    <a
      href="mailto:mukhamikaranja@gmail.com"
      class="text-green-400 border-green-400 border-2 px-6 py-3 rounded-md hover:bg-green-400 hover:text-white transition duration-300"
    >
      Get In Touch
    </a>
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'HeroSection',
});
</script>

<style scoped>
</style>
