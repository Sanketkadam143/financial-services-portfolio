<template>
    <div class="max-w-7xl  m-auto px-4 md:px-0 mb-10 md:my-0">
        <h2 class="text-4xl font-bold text-center mb-8">Gallery</h2>

  
        <div class="grid grid-cols-2 md:grid-cols-3 gap-4">
  <div v-for="(content, index) in GallerySectionContent.images" :key="index">
    
    <div v-if="content.type === 'pdf'">
      <embed
        v-if="content.type === 'pdf'"
        class="md:h-72 md:w-96 rounded-lg"
        :src="content.src"
        type="application/pdf"
        width="100%"
        height="100%"
      />
    </div>
    <div v-else>
      <img
        v-if="content.type === 'image'"
        class="md:h-72 md:w-96 rounded-lg"
        :src="content.src"
        :alt="content.alt"
      />
    </div>
  </div>
</div>

</div>
  </template>
  
  <script setup lang="ts">
  import { GallerySectionContent } from '../constant';
  </script>
  