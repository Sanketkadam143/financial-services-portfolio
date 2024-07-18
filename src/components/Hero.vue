<!-- src/components/HeroSection.vue -->
<template>
  <div id="home" class="relative bg-cover bg-center flex flex-col md:h-[40rem]" :style="{ backgroundImage: `url(${currentBackground})` }">
    <!-- Background Overlay with Low Opacity -->
    <div class="absolute inset-0 bg-gray-900 bg-opacity-70 z-0"></div>

    <!-- Navbar -->
    <nav class="relative z-10 flex justify-between items-center p-6">
      <div class="flex items-center space-x-4">
        <!-- Logo -->
        <!-- <img :src="icon1" alt="logo" /> -->
        <!-- <img :src="NavbarContent.logo" alt="NavbarContent.logo"/> -->
        <!-- Nav Links (Left) -->
        <div class="hidden md:flex space-x-4">
          <a href="#home" class="text-white hover:text-gray-300">Home</a>
          <a href="#service" class="text-white hover:text-gray-300">Our Services</a>
          <a href="#about" class="text-white hover:text-gray-300">About Us</a>
        </div>
      </div>
      <!-- Nav Links (Right) -->
      <div class="hidden md:flex items-center space-x-4">
        <a href="#whyus" class="text-white hover:text-gray-300">Why Us</a>
        <a href="#testimonial" class="text-white hover:text-gray-300">Testimonial</a>
        <a href="#contact" class="text-white hover:text-gray-300">Contact</a>
        <!-- <button class="bg-blue-700 text-white px-4 py-2 rounded-full hover:bg-blue-700">Get Started</button> -->
      </div>
      <!-- Mobile Menu Button -->
      <button @click="toggleMenu" class="md:hidden text-white">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" class="w-6 h-6">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
        </svg>
      </button>
    </nav>

  <!-- Mobile Menu -->
  <div v-if="isMenuOpen" class="md:hidden bg-gray-800 bg-opacity-90 p-6 absolute inset-0 z-20 flex flex-col items-center space-y-4">
      <button @click="toggleMenu" class="absolute top-4 right-4 text-white">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" class="w-6 h-6">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
      <a href="#home" class="text-white hover:text-gray-300">Home</a>
      <a href="#service" class="text-white hover:text-gray-300">Our Services</a>
      <a href="#about" class="text-white hover:text-gray-300">About Us</a>
      <a href="#testimonial" class="text-white hover:text-gray-300">Testimonial</a>
      <a href="#whyus" class="text-white hover:text-gray-300">Why Us</a>
      <a href="#contact" class="text-white hover:text-gray-300">Contact</a>
      <button class="bg-blue-700 text-white px-6 py-3 my-4 md:my-0 rounded-full hover:bg-blue-500" @click="openWhatsApp">Open Your Demat Account</button>
    </div>

    <!-- Hero Content -->
    <div class="relative z-10 flex flex-1 items-center justify-center text-center py-10 mt-24">
      <div class="text-white">
        <!-- <h1 class="text-9xl font-bold mb-4">JM Financial</h1> -->
        <h1 class="text-5xl font-bold mb-4">Dream High Financial Services</h1>
        <p class="text-xl md:mb-8 md:w-full mx-auto">India's best research, best services and minimun brokerage</p>
        <button class="bg-blue-700 text-white px-6 py-3 my-4 md:my-0 rounded-full hover:bg-blue-500"  @click="openWhatsApp" >Open Your Demat Account</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isMenuOpen: false,
      currentBackground: 'https://gaadibaazar.s3.ap-south-1.amazonaws.com/media/client_media/1000058867-01_qGNSI_1719228837.0.jpeg',
      backgrounds: [
        'https://images.unsplash.com/photo-1560221328-12fe60f83ab8?q=80&w=2948&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
        'https://images.unsplash.com/photo-1612010167108-3e6b327405f0?q=80&w=2940&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
        'https://gaadibaazar.s3.ap-south-1.amazonaws.com/media/client_media/1000058867-01_qGNSI_1719228837.0.jpeg'
      ],
      currentBackgroundIndex: 0
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
    changeBackground() {
      this.currentBackgroundIndex = (this.currentBackgroundIndex + 1) % this.backgrounds.length;
      this.currentBackground = this.backgrounds[this.currentBackgroundIndex];
    },
    openWhatsApp() {
      const phoneNumber = '917576919191'; // replace with your WhatsApp phone number
      const message = 'Hello! I want to open my demat account'; // replace with your default message
      window.open(`https://wa.me/${phoneNumber}?text=${encodeURIComponent(message)}`, '_blank');
    }
  },
  mounted() {
    setInterval(this.changeBackground, 2000); // Change background every 5 seconds
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

/* Smooth background image transition */
#home {
  transition: background-image 1s ease-in-out;
}
</style>
