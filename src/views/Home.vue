<template>
  <section
    class="w-full h-screen relative bg-cover bg-center flex flex-col text-white"
    :style="{ backgroundImage: `url(${heroImage})` }"
  >
    <div class="absolute inset-0 bg-black bg-opacity-40"></div>

    <div class="relative z-20">
      <Navbar />
    </div>

    <div
      class="relative z-10 flex flex-col justify-center items-center text-center px-4 flex-grow"
    >
      <h1 class="text-5xl font-bold mb-4">Welcome to Remo Comp</h1>
      <p class="text-xl mb-6 max-w-xl">
        We bring the best to your home with professional remodeling services.
      </p>
      <router-link
        to="/services"
        class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-3 rounded-lg font-semibold"
      >
        Get Started
      </router-link>
    </div>
  </section>
</template>

<script>
import heroImage from "../assets/images/cloudy_city.jpg";
import Navbar from "../components/Navbar.vue";

export default {
  components: { Navbar },
  data() {
    return { heroImage };
  },
};
</script>
