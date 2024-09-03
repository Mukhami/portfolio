<template>
  <section id="experience" class="bg-inherit py-20 text-white w-full">
    <div class="container mx-auto px-6 md:px-12 lg:px-20 w-full">
      <div class="w-full">
        <h2 class="text-3xl font-bold mb-6 tracking-tight sm:text-4xl">Where I have worked</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
          <article v-for="post in workplaces" :key="post.id" class="flex max-w-xl flex-col items-start justify-between">
            <div class="flex items-center gap-x-4 text-xs">
              <p>{{ post.date }}</p>
              <p class="relative z-10 rounded-full bg-gray-50 px-3 py-1.5 font-medium text-gray-600 hover:bg-gray-100">{{ post.role.title }}</p>
            </div>
            <div class="group relative">
              <h3 class="mt-3 text-lg font-semibold leading-6 group-hover:text-green-400">
                <a :href="post.href">
                  <span class="absolute inset-0" />
                  {{ post.title }}
                </a>
              </h3>
              <p class="mt-5 text-sm leading-6">{{ post.description }}</p>
            </div>
            <div class="mt-4 flex flex-wrap gap-2 text-xs">
              <span v-for="tech in post.stack" :key="tech" class="cursor-pointer relative z-10 rounded-full bg-inherit px-2 py-1.5 font-medium text-green-400 border-green-400 border">
                {{ tech }}
              </span>
            </div>
          </article>
        </div>
      </div>
    </div>
  </section>
</template>


<script setup lang="js">
const workplaces = [
  {
    id: 1,
    title: 'Co-foundry',
    description: "As a full-stack developer at Co-Foundry, I focus on building custom components within our Laravel-based framework, using VueJS and TypeScript. I’ve also leveraged the framework to create detailed dashboards and reports, delivering tailored solutions that meet our clients' needs.",
    date: '2023 - Present',
    role: { title: 'Fullstack Software Developer'},
    stack: ['Laravel', 'VueJS', 'MySQL', 'Docker', 'TypeScript'],
  },
  {
    id: 2,
    title: 'AirDuka',
    description: "At AirDuka, I led the migration from CodeIgniter to Laravel, optimizing system performance and security while integrating Algolia for faster searches and enhancing customer engagement. I implemented payment gateways and logistics metrics for seamless checkouts and accurate shipping costs. I also created sprint documentation, contributed to e-commerce development, and collaborated with cross-functional teams to deliver high-quality, scalable solutions that aligned with business goals.",
    date: '2021 - 2023',
    role: { title: 'Senior Software Developer'},
    stack: ['CodeIgniter', 'Laravel', 'MySQL', 'LiveWire', 'Algolia', 'Javascript'],
  },
  {
    id: 3,
    title: 'Deveint Limited',
    description: "I implemented and maintained software systems across industries like Loan Management, Lottery Generation, Guest Management, and E-Commerce, ensuring optimal performance and aligning client needs with effective solutions. I specialized in PHP-based web applications using CodeIgniter or Laravel, with HTML, CSS, and JavaScript for front-end development. I also assigned tasks to interns and handled server configurations for deployments.",
    date: '2019 - 2021',
    role: { title: 'Software Developer'},
    stack: ['PHP', 'HTML', 'CSS', 'Javascript', 'jQuery', 'CodeIgniter', 'Laravel', 'Postgres'],
  },
]
</script>
