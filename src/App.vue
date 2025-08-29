<template>
  <div class="relative min-h-screen">
    <!-- Hero section with overlay and background -->
    <section
      class="w-full h-screen relative bg-cover bg-center flex flex-col text-white"
      :style="{ backgroundImage: `url(${heroImage})` }"
    >
      <!-- Overlay -->
      <div class="absolute inset-0 bg-black bg-opacity-40"></div>

      <!-- Navbar -->
      <div class="relative z-20">
        <Navbar />
      </div>

      <!-- Hero content -->
      <div
        class="relative z-10 flex flex-col justify-center items-center text-center px-4 flex-grow"
      >
        <h1 class="text-5xl font-bold mb-4">Welcome to CompName</h1>
        <p class="text-xl mb-6 max-w-xl">
          We bring brilliance to your home with professional remodeling services.
        </p>
        <a
          href="/contact"
          class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-3 rounded-lg font-semibold"
        >
          Get Started
        </a>
      </div>
    </section>

    <!-- Footer -->
    <Footer />
  </div>
</template>


<script>
import Navbar from "./components/Navbar.vue";
import Footer from "./components/Footer.vue";
import heroImage from "./assets/images/cloudy_city.jpg"; 

export default {
  components: {
    Navbar,
    Footer,
  },
  data() {
    return {
      heroImage, 
    };
  },
};
</script>
