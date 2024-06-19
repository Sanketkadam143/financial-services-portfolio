<template>
  <div id="about" class="my-10 max-w-7xl mx-auto">
    <div class="flex justify-center">
      <img :src="AboutSectionContent.AboutUsImage" class="w-full object-cover h-80" />
    </div>
    <div class="flex flex-col justify-center my-10">
      <h1 class="text-center text-4xl font-bold">
        {{ AboutSectionContent.AboutUsHeading }}
      </h1>
      <p class="text-center text-xl mt-4">
        {{ AboutSectionContent.AboutUsSubHeading }}
      </p>
    </div>
    
    <div class="grid grid-cols-1 md:grid-cols-2 gap-4 px-5">
      <div 
        v-for="(section, index) in AboutSectionContent.AboutUsDescription"
        :key="index"
        class="px-8 py-12 mx-auto space-y-4 bg-white border rounded-lg shadow-lg"
      >
        <h2 class="space-y-1 text-2xl font-bold leading-none text-gray-900">
          <span class="block text-lg text-blue-700">{{section.title}}</span>
        </h2>
        <p>
          {{ section.content }}
        </p>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { AboutSectionContent } from '../constant';
</script>
