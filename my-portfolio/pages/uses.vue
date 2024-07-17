<template>
    <section class="container mx-auto py-8">
      <h1 class="text-4xl font-bold mb-4">Uses</h1>
      <div class="space-y-4">
        <NuxtLink v-for="item in uses" :key="item.id" :to="'/uses/' + item.slug" 
                  class="block border p-4 rounded-md shadow-md hover:bg-gray-100 active:bg-gray-200">
          <h2 class="text-2xl font-bold">{{ item.name }}</h2>
          <p class="text-gray-700">{{ item.description }}</p>
        </NuxtLink>
      </div>
    </section>
  </template>
  
  <script setup>
  const uses = [
    { id: 1, name: 'Laptop', description: 'Dell Laptop, sponsored by University', slug: 'laptop' },
    { id: 2, name: 'Editor', description: 'OBS, Figma, Canva, and many more editing apps that i can use', slug: 'editor' },
  ];
  </script>
  