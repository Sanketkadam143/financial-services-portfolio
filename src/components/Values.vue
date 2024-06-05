<template>
    <section class="max-w-7xl mx-auto my-t-5 mb-20">
      <h2 class="text-3xl font-bold text-center mb-8">Our Values</h2>
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
        <div v-for="(value, index) in ourValues" :key="index" class="flex flex-col items-center">
          <img :src="value.image" alt="Value Image" class="w-24 h-24 mb-4" />
          <h3 class="text-xl font-semibold">{{ value.title }}</h3>
        </div>
      </div>
    </section>
  </template>
  
  <script setup lang="ts">
 import { ourValues } from '../constant';
  </script>
  
  <style scoped>
  /* Custom styles if needed */
  </style>
  