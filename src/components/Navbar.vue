<template>
  <header
    :class="['fixed w-full z-50 transition-all duration-300', scrolled ? 'bg-white shadow-md' : 'bg-transparent']">

    <!-- Top info bar -->
    <div :class="['text-lg py-6 relative z-30 transition-colors duration-300', scrolled ? 'text-black' : 'text-white']">
      <div class="max-w-screen-xl mx-auto px-4 sm:px-6 lg:px-8 
       flex flex-row flex-wrap items-center 
       justify-center md:justify-between 
       text-center md:text-left space-y-0 space-x-6">

        <!-- Left side (Location + Phone) -->
        <div class="flex flex-row items-center space-x-6">
          <div class="flex items-center space-x-3">
            <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" fill="currentColor"
              class="bi bi-geo-alt-fill" viewBox="0 0 16 16">
              <path d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10m0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6" />
            </svg>
            <span>Houston, TX</span>
          </div>
          <div class="flex items-center space-x-3">
            <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" fill="currentColor"
              class="bi bi-telephone-fill" viewBox="0 0 16 16">
              <path fill-rule="evenodd"
                d="M1.885.511a1.745 1.745 0 0 1 2.61.163L6.29 2.98c.329.423.445.974.315 1.494l-.547 2.19a.68.68 0 0 0 .178.643l2.457 2.457a.68.68 0 0 0 .644.178l2.189-.547a1.75 1.75 0 0 1 1.494.315l2.306 1.794c.829.645.905 1.87.163 2.611l-1.034 1.034c-.74.74-1.846 1.065-2.877.702a18.6 18.6 0 0 1-7.01-4.42 18.6 18.6 0 0 1-4.42-7.009c-.362-1.03-.037-2.137.703-2.877z" />
            </svg>
            <span>(000) 000-0000</span>
          </div>
        </div>

        <!-- Right side (Availability) -->
        <div class="flex items-center space-x-3 mt-4 md:mt-0">
          <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" fill="currentColor"
            class="bi bi-clock-fill hidden md:inline" viewBox="0 0 16 16">
            <path
              d="M16 8A8 8 0 1 1 0 8a8 8 0 0 1 16 0M8 3.5a.5.5 0 0 0-1 0V9a.5.5 0 0 0 .252.434l3.5 2a.5.5 0 0 0 .496-.868L8 8.71z" />
          </svg>
          <span class="hidden md:inline">Available: Mon-Fri 5:00am - 6:00pm</span>
        </div>
      </div>
    </div>


    <hr
      :class="['transition-colors duration-300', scrolled ? 'border-black border-opacity-20' : 'border-white border-opacity-30']" />

    <!-- Main navbar -->
    <nav class="py-5 relative z-30">
      <div class="max-w-screen-xl mx-auto px-4 sm:px-6 lg:px-8 flex items-center justify-between">

        <!-- Logo -->
        <router-link
          :class="['flex items-center space-x-3 font-bold text-4xl transition-colors duration-300', scrolled ? 'text-black' : 'text-white']"
          to="/">
          REMO COMP
        </router-link>

        <!-- Desktop links -->
        <ul :class="['hidden lg:flex relative text-base lg:text-lg space-x-4 lg:space-x-5 xl:space-x-12 transition-colors duration-300', scrolled ? 'text-black' : 'text-white']">

          <li><router-link to="/" class="hover:text-blue-400">HOME</router-link></li>
          <li><router-link to="/about" class="hover:text-blue-400">ABOUT US</router-link></li>

          <!-- Services with dropdown -->
          <li class="relative group">
            <button class="hover:text-blue-400 flex items-center space-x-1 focus:outline-none">
              <span>SERVICES</span>
              <svg class="h-4 w-4 transform group-hover:rotate-180 transition" fill="none" stroke="currentColor"
                viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
              </svg>
            </button>
            <ul
              class="absolute left-0 mt-0 w-44 bg-black bg-opacity-90 text-white rounded-lg shadow-lg opacity-0 invisible group-hover:opacity-100 group-hover:visible transition duration-200">
              <li><router-link to="/services/residential"
                  class="block px-4 py-2 hover:bg-blue-600">Kithchen</router-link></li>
              <li><router-link to="/services/commercial"
                  class="block px-4 py-2 hover:bg-blue-600">Bathroom</router-link></li>
              <li><router-link to="/services/deep-cleaning" class="block px-4 py-2 hover:bg-blue-600">Living
                  Spaces</router-link></li>
              <li><router-link to="/services/deep-cleaning" class="block px-4 py-2 hover:bg-blue-600">Outdoor
                  Spaces</router-link></li>
              <li><router-link to="/services/deep-cleaning" class="block px-4 py-2 hover:bg-blue-600">Room
                  Additions</router-link></li>
              <li><router-link to="/services/deep-cleaning" class="block px-4 py-2 hover:bg-blue-600">Whole House
                  Remodels</router-link></li>
              <li><router-link to="/services/deep-cleaning" class="block px-4 py-2 hover:bg-blue-600">Maintanence &
                  Repair</router-link></li>
              <li><router-link to="/services/deep-cleaning"
                  class="block px-4 py-2 hover:bg-blue-600">Carpentry</router-link></li>
              <li><router-link to="/services/deep-cleaning"
                  class="block px-4 py-2 hover:bg-blue-600">Drywall</router-link></li>
              <li><router-link to="/services/deep-cleaning"
                  class="block px-4 py-2 hover:bg-blue-600">Electrical</router-link></li>
              <li><router-link to="/services/deep-cleaning"
                  class="block px-4 py-2 hover:bg-blue-600">Plumbing</router-link></li>
              <li><router-link to="/services/deep-cleaning"
                  class="block px-4 py-2 hover:bg-blue-600">Roofing</router-link></li>
              <li><router-link to="/services/deep-cleaning"
                  class="block px-4 py-2 hover:bg-blue-600">Landscaping</router-link></li>
              <li><router-link to="/services/deep-cleaning"
                  class="block px-4 py-2 hover:bg-blue-600">Fence</router-link></li>
            </ul>
          </li>

          <!-- Projects dropdown -->
          <li class="relative group">
            <button class="hover:text-blue-400 flex items-center space-x-1 focus:outline-none">
              <span>PROJECTS</span>
              <svg class="h-4 w-4 transform group-hover:rotate-180 transition" fill="none" stroke="currentColor"
                viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
              </svg>
            </button>
            <ul
              class="absolute left-0 mt-0 w-44 bg-black bg-opacity-90 text-white rounded-lg shadow-lg opacity-0 invisible group-hover:opacity-100 group-hover:visible transition duration-200">
              <li><router-link to="/projects/residential" class="block px-4 py-2 hover:bg-blue-600">Indoor
                  Remodels</router-link></li>
              <li><router-link to="/projects/commercial" class="block px-4 py-2 hover:bg-blue-600">Outdoor
                  Remodels</router-link></li>
            </ul>
          </li>

          <li><router-link to="/contact" class="hover:text-blue-400">CONTACT</router-link></li>
        </ul>

        <!-- Mobile hamburger -->
        <button :class="['lg:hidden focus:outline-none z-40 transition-colors duration-300', scrolled ? 'text-black' : 'text-white']" @click="isOpen = !isOpen">

          <svg v-if="!isOpen" xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24"
            stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
          </svg>
          <svg v-else xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24"
            stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
          </svg>
        </button>
      </div>

      <!-- Backdrop overlay -->
      <transition name="fade">
        <div v-if="isOpen" @click="isOpen = false" class="fixed inset-0 bg-black/30 backdrop-blur-sm z-40 lg:hidden">
        </div>
      </transition>

      <!-- Mobile Off-Canvas Menu -->
      <transition name="slide">
        <div v-show="isOpen" class="fixed top-0 right-0 h-full w-11/12 sm:w-3/4 md:w-2/3 lg:w-1/2 
           bg-white text-black px-6 py-6 space-y-4 z-50
           transform transition-transform duration-300 ease-in-out 
           overflow-y-auto">

          <!-- Close button -->
          <button @click="isOpen = false" class="absolute top-4 right-4 text-3xl font-bold text-black">&times;</button>

          <router-link to="/" class="block text-lg hover:text-blue-600">Home</router-link>
          <router-link to="/about" class="block text-lg hover:text-blue-600">About</router-link>

          <!-- Services toggle -->
          <div>
            <button @click="isServicesOpen = !isServicesOpen"
              class="flex justify-between items-center w-full text-lg hover:text-blue-600 focus:outline-none">
              <span>Services</span>
              <svg class="h-5 w-5 transform transition" :class="{ 'rotate-180': isServicesOpen }" fill="none"
                stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
              </svg>
            </button>
            <div v-if="isServicesOpen" class="mt-2 ml-4 space-y-2 text-sm">
              <router-link to="/services/residential" class="block px-4 py-2 hover:bg-blue-600">- Kithchen</router-link>
              <router-link to="/services/commercial" class="block px-4 py-2 hover:bg-blue-600">- Bathroom</router-link>
              <router-link to="/services/deep-cleaning" class="block px-4 py-2 hover:bg-blue-600">- Living
                Spaces</router-link>
              <router-link to="/services/deep-cleaning" class="block px-4 py-2 hover:bg-blue-600">- Outdoor
                Spaces</router-link>
              <router-link to="/services/deep-cleaning" class="block px-4 py-2 hover:bg-blue-600">- Room
                Additions</router-link>
              <router-link to="/services/deep-cleaning" class="block px-4 py-2 hover:bg-blue-600">- Whole House
                Remodels</router-link>
              <router-link to="/services/deep-cleaning" class="block px-4 py-2 hover:bg-blue-600">- Maintanence &
                Repair</router-link>
              <router-link to="/services/deep-cleaning" class="block px-4 py-2 hover:bg-blue-600">-
                Flooring</router-link>
              <router-link to="/services/deep-cleaning" class="block px-4 py-2 hover:bg-blue-600">-
                Drywall</router-link>
              <router-link to="/services/deep-cleaning" class="block px-4 py-2 hover:bg-blue-600">-
                Electrical</router-link>
              <router-link to="/services/deep-cleaning" class="block px-4 py-2 hover:bg-blue-600">-
                Plumbing</router-link>
              <router-link to="/services/deep-cleaning" class="block px-4 py-2 hover:bg-blue-600">-
                Roofing</router-link>
              <router-link to="/services/deep-cleaning" class="block px-4 py-2 hover:bg-blue-600">-
                Landscaping</router-link>
              <router-link to="/services/deep-cleaning" class="block px-4 py-2 hover:bg-blue-600">- Fence</router-link>

            </div>
          </div>

          <!-- Projects toggle -->
          <div>
            <button @click="isProjectsOpen = !isProjectsOpen"
              class="flex justify-between items-center w-full text-lg hover:text-blue-600 focus:outline-none">
              <span>Projects</span>
              <svg class="h-5 w-5 transform transition" :class="{ 'rotate-180': isProjectsOpen }" fill="none"
                stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
              </svg>
            </button>
            <div v-if="isProjectsOpen" class="mt-2 ml-4 space-y-2 text-sm">
              <router-link to="/projects/residential" class="block hover:text-blue-600">- Indoor Remodels</router-link>
              <router-link to="/projects/commercial" class="block hover:text-blue-600">- Outdoor Remodels</router-link>
            </div>
          </div>

          <router-link to="/contact" class="block text-lg hover:text-blue-600">Contact</router-link>
        </div>
      </transition>
    </nav>
  </header>
</template>


<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

.slide-enter-active,
.slide-leave-active {
  transition: transform 0.3s ease-in-out;
}

.slide-enter-from,
.slide-leave-to {
  transform: translateX(100%);
}
</style>


<script>
export default {
  name: "Navbar",
  data() {
    return {
      isOpen: false,
      isServicesOpen: false,
      isProjectsOpen: false,
      scrolled: false // <-- NEW
    };
  },
  watch: {
    isOpen(newVal) {
      if (newVal) {
        document.body.classList.add("overflow-hidden");
      } else {
        document.body.classList.remove("overflow-hidden");
      }
    }
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
  beforeUnmount() {
    window.removeEventListener("scroll", this.handleScroll);
  },
  methods: {
    handleScroll() {
      this.scrolled = window.scrollY > 50; // adjust threshold if needed
    }
  }
};
</script>
