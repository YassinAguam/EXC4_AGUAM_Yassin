<script setup>
const projects = [
  { id: 1, title: 'KASABA App', description: 'A Maranaw translator app to help non-Maranao speakers understand the basic language.', slug: 'kasaba-app' },
  { id: 2, title: 'GYM App', description: 'An app to help you reach your fitness goals!', slug: 'gym-app' },
];
</script>

<template>
  <section class="container mx-auto py-12 px-4">
    <h1 class="text-4xl font-bold mb-8 text-gray-900">Projects</h1>
    <p class="text-lg text-gray-700 mb-10">Here are some of the projects I have worked on. Each project highlights a unique solution to a specific problem, showcasing my skills and expertise in software development.</p>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
      <NuxtLink v-for="project in projects" :key="project.id" :to="'/projects/' + project.slug" class="block border border-gray-200 p-6 rounded-lg shadow-lg hover:shadow-xl transition-shadow duration-300 ease-in-out">
        <h2 class="text-2xl font-bold text-gray-800">{{ project.title }}</h2>
        <p class="text-gray-600 mt-2">{{ project.description }}</p>
      </NuxtLink>
    </div>
  </section>
</template>

<style scoped>
h1 {
  color: #1a202c;
}
h2 {
  color: #2c5282;
}
p {
  font-size: 1rem;
  line-height: 1.5rem;
}
</style>
