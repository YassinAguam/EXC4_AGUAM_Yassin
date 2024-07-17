<template>
    <section class="container mx-auto py-8">
      <h1 class="text-4xl font-bold mb-4">Blog</h1>
      <div class="space-y-4">
        <NuxtLink v-for="post in posts" :key="post.id" :to="'/blog/' + post.slug" 
                  class="block border p-4 rounded-md shadow-md hover:bg-gray-100 active:bg-gray-200">
          <h2 class="text-2xl font-bold">{{ post.title }}</h2>
          <p class="text-gray-700">{{ post.excerpt }}</p>
        </NuxtLink>
      </div>
    </section>
  </template>
  
  <script setup>
  const posts = [
    { id: 1, title: 'First Post', excerpt: 'This is my first code blog post.', slug: 'first-post' },
    { id: 2, title: 'Second Post', excerpt: 'This is my second code blog post.', slug: 'second-post' },
  ];
  </script>
  