<template>
    <div class="  text-white">

   
    <div class="max-w-7xl mx-auto my-20 py-10 px-5 bg-gradient-to-r from-blue-500 to-blue-900 md:rounded-3xl">
 
     <div>
         <h2 class="text-4xl font-bold text-center mb-8">Why Us</h2>
     </div>
 
     <div class="md:flex justify-evenly">
         <div v-for="(section , index) in WhyUSSectionContent.descriptions"
         :key="index"
         class="md:w-1/3 my-10 md:my-0"
         >
             <div class="">
                 <img :src="section.imageSrc"
                    class="w-24 h-24 rounded-lg mx-auto"
                 />
             </div>
             <div class="text-center">
                 <p class="my-4 md:w-3/4 mx-auto"> {{ section.description }}
                </p>
             </div>
         </div>
    
     </div>
 
    </div>  </div>
   </template>
   
   <script setup lang="ts">
   import { WhyUSSectionContent } from '../constant';
   </script>
   
   <style>
   body {
     margin: 0;
     font-family: Arial, sans-serif;
   }
   </style>
   