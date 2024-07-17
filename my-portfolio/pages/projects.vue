<template>
    <section class="container mx-auto py-8">
      <h1 class="text-4xl font-bold mb-4">Projects</h1>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <NuxtLink v-for="project in projects" :key="project.id" :to="'/projects/' + project.slug" 
                  class="block border p-4 rounded-md shadow-md hover:bg-gray-100 active:bg-gray-200">
          <h2 class="text-2xl font-bold">{{ project.title }}</h2>
          <p class="text-gray-700">{{ project.description }}</p>
        </NuxtLink>
      </div>
    </section>
  </template>
  
  <script setup>
  const projects = [
    { id: 1, title: 'Project One', description: 'KASABA App - "a meranaw translater app".', slug: 'project-one' },
    { id: 2, title: 'Project Two', description: 'GYM App -"an app to reach your fitness goal!".', slug: 'project-two' },
  ];
  </script>
  