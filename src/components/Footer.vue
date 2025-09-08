<template>
  <footer class="bg-gray-800 text-white py-10 mt-auto">
    <div
      class="max-w-screen-xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col md:flex-row justify-between space-y-8 md:space-y-0">

      <!--  Company n Social -->
      <div class="md:w-1/2 text-center md:text-left space-y-4">
        <div class="text-2xl font-bold">REMO COMP</div>
        <p class="text-gray-400 text-sm md:text-base md:w-4/5">
          REMO COMP is your trusted partner in remodeling and construction. We deliver high-quality services for
          residential and commercial projects with professionalism and care.
        </p>
        <!-- Social Icons -->
        <div class="mt-4 flex justify-center md:justify-start space-x-6">
          <a href="#" class="hover:text-blue-500" aria-label="Facebook">
            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
              <path
                d="M22 12c0-5.522-4.477-10-10-10S2 6.478 2 12c0 4.991 3.657 9.128 8.438 9.879v-6.987h-2.54v-2.892h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.464h-1.26c-1.243 0-1.63.771-1.63 1.562v1.875h2.773l-.443 2.892h-2.33v6.987C18.343 21.128 22 16.991 22 12z" />
            </svg>
          </a>
          <a href="#" class="hover:text-blue-400" aria-label="Twitter">
            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
              <path
                d="M22.46 6c-.77.35-1.5.58-2.34.69a4.1 4.1 0 001.81-2.27 8.2 8.2 0 01-2.6.99 4.1 4.1 0 00-7 3.74A11.65 11.65 0 013 4.89a4.1 4.1 0 001.27 5.47 4.08 4.08 0 01-1.86-.51v.05a4.1 4.1 0 003.29 4 4.1 4.1 0 01-1.85.07 4.1 4.1 0 003.83 2.85A8.22 8.22 0 012 19.54 11.6 11.6 0 008.29 21c7.55 0 11.68-6.25 11.68-11.67 0-.18 0-.36-.01-.53A8.3 8.3 0 0022.46 6z" />
            </svg>
          </a>
          <a href="#" class="hover:text-pink-500" aria-label="Instagram">
            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
              <path
                d="M12 2.2c3.2 0 3.584.012 4.85.07 1.17.055 1.97.24 2.42.4a4.9 4.9 0 011.76 1.15 4.9 4.9 0 011.15 1.76c.16.45.345 1.25.4 2.42.058 1.27.07 1.65.07 4.85s-.012 3.584-.07 4.85c-.055 1.17-.24 1.97-.4 2.42a4.9 4.9 0 01-1.15 1.76 4.9 4.9 0 01-1.76 1.15c-.45.16-1.25.345-2.42.4-1.27.058-1.65.07-4.85.07s-3.584-.012-4.85-.07c-1.17-.055-1.97-.24-2.42-.4a4.9 4.9 0 01-1.76-1.15 4.9 4.9 0 01-1.15-1.76c-.16-.45-.345-1.25-.4-2.42C2.212 15.584 2.2 15.2 2.2 12s.012-3.584.07-4.85c.055-1.17.24-1.97.4-2.42a4.9 4.9 0 011.15-1.76 4.9 4.9 0 011.76-1.15c.45-.16 1.25-.345 2.42-.4C8.416 2.212 8.8 2.2 12 2.2zm0-2.2C8.74 0 8.332.012 7.052.07 5.77.127 4.802.308 4.042.553a7.1 7.1 0 00-2.57 1.51A7.1 7.1 0 00.553 4.042c-.245.76-.426 1.728-.483 3.01C.012 8.332 0 8.74 0 12s.012 3.668.07 4.948c.057 1.282.238 2.25.483 3.01a7.1 7.1 0 001.51 2.57 7.1 7.1 0 002.57 1.51c.76.245 1.728.426 3.01.483C8.332 23.988 8.74 24 12 24s3.668-.012 4.948-.07c1.282-.057 2.25-.238 3.01-.483a7.1 7.1 0 002.57-1.51 7.1 7.1 0 001.51-2.57c.245-.76.426-1.728.483-3.01.058-1.28.07-1.688.07-4.948s-.012-3.668-.07-4.948c-.057-1.282-.238-2.25-.483-3.01a7.1 7.1 0 00-1.51-2.57 7.1 7.1 0 00-2.57-1.51c-.76-.245-1.728-.426-3.01-.483C15.668.012 15.26 0 12 0z" />
              <path
                d="M12 5.838a6.162 6.162 0 106.162 6.162A6.162 6.162 0 0012 5.838zm0 10.162a3.999 3.999 0 110-7.998 3.999 3.999 0 010 7.998z" />
              <circle cx="18.406" cy="5.594" r="1.44" />
            </svg>
          </a>
        </div>
      </div>

      <!--Quick Links -->
      <div class="md:w-1/2 text-center md:text-right space-y-4">
        <h3 class="text-lg font-semibold">Quick Links</h3>
        <ul class="flex flex-col md:flex-row justify-center md:justify-end space-y-2 md:space-y-0 md:space-x-6">
          <li><router-link to="/" class="hover:text-blue-400">Home</router-link></li>
          <li><router-link to="/about" class="hover:text-blue-400">About</router-link></li>
          <li><router-link to="/services" class="hover:text-blue-400">Services</router-link></li>
          <li><router-link to="/projects" class="hover:text-blue-400">Projects</router-link></li>
          <li><router-link to="/contact" class="hover:text-blue-400">Contact</router-link></li>
        </ul>
      </div>


    </div>

    <!-- Copyright -->
    <div class="mt-8 text-center text-sm text-gray-400">
      &copy; 2025 REMO COMP. All rights reserved.
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>
