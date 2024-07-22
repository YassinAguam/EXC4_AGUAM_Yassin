<script setup>
import { Icon } from '@iconify/vue';

const links = [
  { name: 'GitHub', href: 'https://github.com', icon: 'entypo-social:github-with-circle' },
  { name: 'Twitter', href: 'https://twitter.com', icon: 'entypo-social:twitter' },
  { name: 'Facebook', href: 'https://facebook.com', icon: 'entypo-social:facebook' },
  { name: 'LinkedIn', href: 'https://www.linkedin.com', icon: 'entypo-social:linkedin-with-circle' },
  { name: 'Instagram', href: 'https://instagram.com', icon: 'entypo-social:instagram' }
];
</script>

<template>
  <footer class="bg-gray-900 text-gray-300 py-6">
    <div class="container mx-auto flex flex-col items-center md:flex-row justify-between">
      <p class="mb-4 md:mb-0">&copy; 2024 Yassin A. Aguam. All Rights Reserved.</p>
      <div class="flex gap-4">
        <a v-for="link in links" :key="link.name" :href="link.href" target="_blank" rel="noopener noreferrer">
          <Icon :icon="link.icon" width="24" height="24" class="text-gray-300 hover:text-white" />
        </a>
      </div>
    </div>
  </footer>
</template>
