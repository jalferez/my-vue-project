<template>
  <header class="w-full">
    
    <!-- Top info bar -->
    <div class="bg-transparent text-white text-sm flex items-center space-x-6 px-6 py-2 relative z-20">
      <div class="flex items-center space-x-1">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 text-white" fill="none" viewBox="0 0 24 24"
          stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
            d="M12 11c1.38 0 2.5-1.12 2.5-2.5S13.38 6 12 6s-2.5 1.12-2.5 2.5S10.62 11 12 11z" />
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
            d="M12 22s8-4.5 8-11a8 8 0 10-16 0c0 6.5 8 11 8 11z" />
        </svg>
        <span>Houston, TX</span>
      </div>
      <div class="flex items-center space-x-1">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 text-white" fill="none" viewBox="0 0 24 24"
          stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
            d="M3 5a2 2 0 012-2h2a2 2 0 012 2v3a2 2 0 01-2 2H5a2 2 0 01-2-2V5zM16 3h5v5m0 0L16 3m5 5l-5-5M16 16h5v5m0 0L16 16m5 5l-5-5" />
        </svg>
        <span>(000) 000-0000</span>
      </div>
    </div>

    <!-- Main navbar -->
    <nav class="bg-transparent px-6 py-4 flex items-center justify-between relative z-20">

      <!-- Logo -->
      <div class="flex items-center space-x-3">
        <img src="../assets/images/logo.png" alt="Logo" class="h-10 w-10" />
        <span class="font-bold text-xl text-white">BrightSpace CL</span>
      </div>

      <!-- Desktop links -->
      <ul class="hidden md:flex space-x-6 text-white relative">
        <li><a href="/" class="hover:text-blue-400">Home</a></li>
        <li><a href="/about" class="hover:text-blue-400">About</a></li>

        <!-- Services with dropdown -->
        <li class="relative group">
          <button class="hover:text-blue-400 flex items-center space-x-1 focus:outline-none">
            <span>Services</span>
            <svg class="h-4 w-4 transform group-hover:rotate-180 transition" fill="none" stroke="currentColor"
              viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
            </svg>
          </button>
          <ul
            class="absolute left-0 -mt-0.5 w-40 bg-black bg-opacity-90 text-white rounded-lg shadow-lg opacity-0 invisible group-hover:opacity-100 group-hover:visible transition duration-200">
            <li>
              <a href="/services/residential" class="block px-4 py-2 hover:bg-blue-600">Residential</a>
            </li>
            <li>
              <a href="/services/commercial" class="block px-4 py-2 hover:bg-blue-600">Commercial</a>
            </li>
            <li>
              <a href="/services/deep-cleaning" class="block px-4 py-2 hover:bg-blue-600">Deep Cleaning</a>
            </li>
          </ul>
        </li>

        <li class="relative group">
          <button class="hover:text-blue-400 flex items-center space-x-1 focus:outline-none">
            <span>Projects</span>
            <svg class="h-4 w-4 transform group-hover:rotate-180 transition" fill="none" stroke="currentColor"
              viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
            </svg>
          </button>
          <ul
            class="absolute left-0 -mt-0.5 w-40 bg-black bg-opacity-90 text-white rounded-lg shadow-lg opacity-0 invisible group-hover:opacity-100 group-hover:visible transition duration-200">
            <li>
              <a href="/projects/residential" class="block px-4 py-2 hover:bg-blue-600">Residential</a>
            </li>
            <li>
              <a href="/projects/commercial" class="block px-4 py-2 hover:bg-blue-600">Commercial</a>
            </li>
            <li>
              <a href="/projects/deep-cleaning" class="block px-4 py-2 hover:bg-blue-600">Deep Cleaning</a>
            </li>
          </ul>
        </li>

        <li><a href="/contact" class="hover:text-blue-400">Contact</a></li>
      </ul>

      <!-- Mobile hamburger -->
      <button @click="isOpen = !isOpen" class="md:hidden text-white focus:outline-none z-30">
        <svg v-if="!isOpen" xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24"
          stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
        </svg>
        <svg v-else xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24"
          stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>

      <!-- Mobile dropdown -->
      <div v-if="isOpen"
        class="absolute top-full left-0 w-full bg-black bg-opacity-90 text-white px-6 py-6 space-y-4 z-20 md:hidden">
        <a href="/" class="block text-lg hover:text-blue-400">Home</a>
        <a href="/about" class="block text-lg hover:text-blue-400">About</a>

        <!-- Services toggle on mobile -->
        <div>
          <button @click="isServicesOpen = !isServicesOpen"
            class="flex justify-between items-center w-full text-lg hover:text-blue-400 focus:outline-none">
            <span>Services</span>
            <svg class="h-5 w-5 transform transition" :class="{ 'rotate-180': isServicesOpen }" fill="none"
              stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
            </svg>
          </button>
          <div v-if="isServicesOpen" class="mt-2 ml-4 space-y-2 text-sm">
            <a href="/services/residential" class="block hover:text-blue-400">Residential</a>
            <a href="/services/commercial" class="block hover:text-blue-400">Commercial</a>
            <a href="/services/deep-cleaning" class="block hover:text-blue-400">Deep Cleaning</a>
          </div>
        </div>

        <div>
          <button @click="isProjectsOpen = !isProjectsOpen"
            class="flex justify-between items-center w-full text-lg hover:text-blue-400 focus:outline-none">
            <span>Projects</span>
            <svg class="h-5 w-5 transform transition" :class="{ 'rotate-180': isProjectsOpen }" fill="none"
              stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
            </svg>
          </button>
          <div v-if="isProjectsOpen" class="mt-2 ml-4 space-y-2 text-sm">
            <a href="/projects/residential" class="block hover:text-blue-400">Residential</a>
            <a href="/projects/commercial" class="block hover:text-blue-400">Commercial</a>
            <a href="/projects/deep-cleaning" class="block hover:text-blue-400">Deep Cleaning</a>
          </div>
        </div>

        <a href="/contact" class="block text-lg hover:text-blue-400">Contact</a>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      isOpen: false, // mobile main menu toggle
      isServicesOpen: false, // mobile services submenu toggle
      isProjectsOpen: false, // mobile projects submenu toggle
    };
  },
};
</script>
