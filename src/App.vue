<template>
  <div class="relative min-h-screen flex flex-col">
    <router-view /> 
    <Footer />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Footer from "./components/Footer.vue";

export default {
  components: { Navbar, Footer },
};
</script>
