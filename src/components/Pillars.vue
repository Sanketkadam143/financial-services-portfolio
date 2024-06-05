<template>
    <div class="max-w-7xl mx-auto  my-10">
        <div class="bg-gradient-to-r from-blue-500 to-blue-900 p-4 rounded-3xl">
            <h2 class="text-white text-3xl text-center my-5 font-semibold">7 Pillars of Excellence</h2>
            <div class="flex flex-col grid-cols-9 p-2 mx-auto md:grid">
                <div v-for="(event, index) in PILLARS" :key="index" :class="index % 2 === 0 ? 'flex md:contents flex-row-reverse' : 'flex md:contents'">
                    <div v-if="index % 2 === 0"
                        class="relative p-4 my-2 text-gray-800 bg-white rounded-xl col-start-1 col-end-5 mr-auto md:mr-0 md:ml-auto">
                        <h3 class="text-lg font-semibold lg:text-xl">{{ event.title }}</h3>
                        <p class="mt-2 leading-6">{{ event.description }}</p>
                    </div>
                    <div class="relative col-start-5 col-end-6 mr-7 md:mx-auto">
                        <div class="flex items-center justify-center w-6 h-full">
                            <div class="w-1 h-full bg-indigo-300 rounded-t-full bg-gradient-to-b from-indigo-400 to-indigo-300"></div>
                        </div>
                        <div class="absolute w-6 h-6 -mt-3 bg-white border-4 border-indigo-400 rounded-full top-1/2"></div>
                    </div>
                    <div v-if="index % 2 !== 0"
                        class="relative p-4 my-2 text-gray-800 bg-white rounded-xl col-start-6 col-end-10 mr-auto">
                        <h3 class="text-lg font-semibold lg:text-xl">{{ event.title }}</h3>
                        <p class="mt-2 leading-6">{{ event.description }}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import { PILLARS } from '../constant';
</script>
