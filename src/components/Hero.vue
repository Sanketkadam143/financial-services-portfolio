<template>
  <div class="relative bg-cover bg-center flex flex-col md:h-[40rem]" :style="{ backgroundImage: `url(https://images.unsplash.com/photo-1560221328-12fe60f83ab8?q=80&w=2948&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D` }">
    <!-- Background Overlay with Low Opacity -->
    <div class="absolute inset-0 bg-gray-900 bg-opacity-70 z-0"></div>
    
    <!-- Navbar -->
    <nav class="relative z-10 flex justify-between items-center p-6">
      <div class="flex items-center space-x-4">
        <!-- Logo -->
        <!-- <img :src="icon1" alt="logo" /> -->
        <!-- <img :src="NavbarContent.logo" alt="NavbarContent.logo"/> -->
        <!-- Toggle Button for Mobile -->
        <button @click="toggleMenu" class="md:hidden text-white focus:outline-none">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
          </svg>
        </button>
        <!-- Nav Links (Left) -->
        <div class="hidden md:flex space-x-4">
          <a href="#" class="text-white hover:text-gray-300">Home</a>
          <a href="#" class="text-white hover:text-gray-300">Our Services</a>
          <a href="#" class="text-white hover:text-gray-300">About Us</a>
        </div>
      </div>
      <!-- Nav Links (Right) -->
      <div class="hidden md:flex items-center space-x-4">
        <a href="#" class="text-white hover:text-gray-300">Testimonial</a>
        <a href="#" class="text-white hover:text-gray-300">Contact</a>
        <button class="bg-blue-700 text-white px-4 py-2 rounded-full hover:bg-blue-700">Get Started</button>
      </div>
    </nav>
    
    <!-- Mobile Menu -->
    <div v-if="menuOpen" class="md:hidden absolute top-16 left-0 right-0 bg-gray-900 bg-opacity-95 text-white flex flex-col space-y-4 p-6 z-20">
      <a href="#" class="hover:text-gray-300">Home</a>
      <a href="#" class="hover:text-gray-300">Our Services</a>
      <a href="#" class="hover:text-gray-300">About Us</a>
      <a href="#" class="hover:text-gray-300">Testimonial</a>
      <a href="#" class="hover:text-gray-300">Contact</a>
      <button class="bg-blue-700 text-white px-4 py-2 rounded-full hover:bg-blue-700">Get Started</button>
    </div>

    <!-- Hero Content -->
    <div class="relative z-10 flex flex-1 items-center justify-center text-center py-10">
      <div class="text-white">
        <h1 class="text-5xl font-bold mb-4">Dream High Financial Services</h1>
        <p class="text-xl md:mb-8 md:w-3/5 mx-auto">Your Professional Financial Advisor</p>
        <button class="bg-blue-700 text-white px-6 py-3 my-4 md:my-0 rounded-full hover:bg-blue-500">Enquire Now</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      menuOpen: false
    };
  },
  methods: {
    toggleMenu() {
      this.menuOpen = !this.menuOpen;
    }
  }
};
</script>

<style scoped>
.h-screen-80 {
  height: 80vh;
}

.bg-cover {
  background-size: cover;
}

.bg-center {
  background-position: center;
}
</style>
