<script setup>
const posts = [
  { id: 1, title: 'Getting Started with Nuxt 3', excerpt: 'Learn the basics of Nuxt 3 and how to set up your first project.', slug: 'getting-started-with-nuxt-3' },
  { id: 2, title: 'Understanding Vue Composition API', excerpt: 'A deep dive into the Composition API and how to use it effectively in your Vue projects.', slug: 'understanding-vue-composition-api' },
];
</script>

<template>
  <section class="container mx-auto py-8 px-4">
    <h1 class="text-4xl font-bold mb-8 text-gray-900">Code Blogs</h1>
    <p class="text-lg text-gray-700 mb-6">Welcome to my coding blog! Here you'll find articles on various web development topics, tutorials, and insights into the world of programming. Happy coding!</p>
    <div class="space-y-6">
      <NuxtLink v-for="post in posts" :key="post.id" :to="'/blog/' + post.slug" class="block border border-gray-200 p-6 rounded-lg shadow-lg hover:bg-gray-100 active:bg-gray-200 transition duration-300">
        <h2 class="text-2xl font-bold text-gray-800">{{ post.title }}</h2>
        <p class="text-gray-600 mt-2">{{ post.excerpt }}</p>
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
