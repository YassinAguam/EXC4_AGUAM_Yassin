<script setup>
import { useRoute } from 'vue-router'

const route = useRoute()
const { slug } = route.params

// Fetch the uses item based on the slug
const useItem = {
  name: 'Sample Item',
  description: `Description of the item with slug ${slug}.`
}
</script>

<template>
  <section class="container mx-auto py-8">
    <h1 class="text-4xl font-bold mb-4">{{ useItem.name }}</h1>
    <p class="text-gray-700">{{ useItem.description }}</p>
  </section>
</template>
