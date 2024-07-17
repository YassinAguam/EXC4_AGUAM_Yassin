<script setup>
import { useRoute } from 'vue-router'

const route = useRoute()
const { slug } = route.params

// Fetch the project based on the slug
const project = {
  title: 'Sample Project',
  description: `Description of the project with slug ${slug}.`
}
</script>

<template>
  <section class="container mx-auto py-8">
    <h1 class="text-4xl font-bold mb-4">{{ project.title }}</h1>
    <p class="text-gray-700">{{ project.description }}</p>
  </section>
</template>
