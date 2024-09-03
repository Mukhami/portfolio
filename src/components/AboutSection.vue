<template>
  <section id="about" class="py-20 text-white">
    <div class="container mx-auto px-6 md:px-12 lg:px-20">
      <div class="flex flex-col md:flex-row items-center">
        <div class="w-full md:w-1/2 mb-8 md:mb-0 md:pr-10">
          <h2 class="text-3xl md:text-4xl font-bold mb-6">About Me</h2>
          <p class="text-sm mb-4">
            Highly skilled and motivated Full-Stack Software Developer with a strong educational background and a passion for creating innovative web applications. A university graduate with expertise in Laravel, PHP, LiveWire, VueJS, and Database Management, demonstrating a proven track record of delivering high-quality solutions that meet both technical and business requirements.
          </p>
          <p class="text-sm mb-4">
            Detail-oriented and well-versed in the entire software development life cycle, adept at collaborating with cross-functional teams to drive project success. Committed to continuous learning and staying up-to-date with the latest technologies to deliver cutting-edge solutions that exceed client expectations.
          </p>
          <p class="text-sm mb-4">
            Seeking opportunities to leverage my technical expertise and creativity in developing robust and user-friendly web applications that make a positive impact on end-users and businesses alike.
          </p>
          <p class="text-sm mb-4">
            Here are a few technologies I’ve been working with recently:
          </p>
          <ul class="grid grid-cols-2 gap-4 text-gray-200 dark:text-gray-100">
            <li> <ChevronDoubleRightIcon class="w-4 h-4 inline text-green-400"/> &nbsp; Laravel</li>
            <li><ChevronDoubleRightIcon class="w-4 h-4 inline text-green-400"/> &nbsp; VueJS</li>
            <li><ChevronDoubleRightIcon class="w-4 h-4 inline text-green-400"/> &nbsp; JavaScript (ES6+)</li>
            <li><ChevronDoubleRightIcon class="w-4 h-4 inline text-green-400"/> &nbsp; TypeScript</li>
            <li><ChevronDoubleRightIcon class="w-4 h-4 inline text-green-400"/> &nbsp; Tailwind CSS</li>
            <li><ChevronDoubleRightIcon class="w-4 h-4 inline text-green-400"/> &nbsp; Node.js</li>
            <li><ChevronDoubleRightIcon class="w-4 h-4 inline text-green-400"/> &nbsp; Docker</li>
            <li><ChevronDoubleRightIcon class="w-4 h-4 inline text-green-400"/> &nbsp; Git Version Control</li>
          </ul>
        </div>
        <div class="w-full md:w-1/2 flex justify-center">
          <img
            src="https://media.licdn.com/dms/image/v2/C4D03AQFrKzovq1jpsQ/profile-displayphoto-shrink_400_400/profile-displayphoto-shrink_400_400/0/1598633321395?e=1730937600&v=beta&t=yuXjDYa9G8cpAYpwwoL1OZFcoot7iB3tgH4TCvC2jag"
            alt="Kevin Mukhami"
            class="rounded-lg shadow-lg w-64 h-64 object-cover"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ArrowLongRightIcon, ChevronDoubleRightIcon } from '@heroicons/vue/16/solid'
</script>

<style scoped>
/* Additional custom styles if needed */
</style>
