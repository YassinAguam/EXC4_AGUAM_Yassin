<script setup>
import { useRoute } from 'vue-router'

const route = useRoute()
const { slug } = route.params

// Fetch the blog post based on the slug
// In a real application, you would fetch data from an API or a data source
const post = {
  title: 'Sample Post',
  content: `Content of the post with slug ${slug}.`
}
</script>

<template>
  <section class="container mx-auto py-8">
    <h1 class="text-4xl font-bold mb-4">{{ post.title }}</h1>
    <p class="text-gray-700">{{ post.content }}</p>
  </section>
</template>
