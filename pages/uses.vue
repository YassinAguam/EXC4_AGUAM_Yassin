<script setup>
const uses = [
  { id: 1, name: 'Dell Laptop', description: 'High-performance laptop sponsored by the University, perfect for development and design tasks.', slug: 'dell-laptop' },
  { id: 2, name: 'Editing Tools', description: 'A suite of tools including OBS, Figma, Canva, and other essential editing applications.', slug: 'editing-tools' },
  { id: 3, name: 'VS Code', description: 'Visual Studio Code is my go-to code editor for development with its vast extensions and features.', slug: 'vs-code' },
  { id: 4, name: 'GitHub', description: 'Platform for version control and collaboration, allowing me to host and review code, manage projects, and build software.', slug: 'github' },
];
</script>

<template>
  <section class="container mx-auto py-12 px-4">
    <h1 class="text-4xl font-bold mb-8 text-gray-900">Tools and Technologies I Use</h1>
    <p class="text-lg text-gray-700 mb-10">Here's a list of the tools and technologies that I use regularly to build, design, and develop my projects. Each tool plays a crucial role in my workflow and helps me achieve my goals efficiently.</p>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
      <NuxtLink v-for="item in uses" :key="item.id" :to="'/uses/' + item.slug" class="block border border-gray-200 p-6 rounded-lg shadow-lg hover:shadow-xl transition-shadow duration-300 ease-in-out">
        <h2 class="text-2xl font-bold text-gray-800">{{ item.name }}</h2>
        <p class="text-gray-600 mt-2">{{ item.description }}</p>
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
