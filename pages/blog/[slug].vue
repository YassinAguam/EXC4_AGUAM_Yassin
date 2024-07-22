<script setup>
import { useRoute } from 'vue-router';

const route = useRoute();
const { slug } = route.params;

const post = ref({
  title: 'Sample Post',
  content: `Content of the post with slug ${slug}.`
});
</script>

<template>
  <section class="container mx-auto py-8">
    <h1 class="text-4xl font-bold mb-4">{{ post.title }}</h1>
    <p class="text-gray-700">{{ post.content }}</p>
  </section>
</template>
