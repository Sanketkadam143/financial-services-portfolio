<template>
    <div class="max-w-7xl  m-auto px-4 md:px-0 mb-10 md:my-0">
        <h2 class="text-4xl font-bold text-center mb-8">Gallery</h2>

  
    <div class="grid grid-cols-2 md:grid-cols-3 gap-4">
      <div v-for="(image, index) in GallerySectionContent.images" :key="index">
        <img class="md:h-72 md:w-96 rounded-lg" :src="image.src" :alt="image.alt" />
      </div>
    </div>
</div>
  </template>
  
  <script setup lang="ts">
  import { GallerySectionContent } from '../constant';
  </script>
  