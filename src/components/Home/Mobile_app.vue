<template>
  <section
    class="relative w-full bg-cover bg-center text-white"
    style="background-image: url('/Home/Fly_Nepal_Airlines.png')"
  >
    <!-- Overlay -->
    <div class="absolute inset-0 bg-black bg-opacity-50"></div>

    <!-- Content Wrapper -->
    <div
      class="relative container mx-auto px-4 sm:px-6 lg:px-20 py-16 flex flex-col md:flex-row items-center md:items-start gap-10"
    >
      <!-- Text Content -->
      <div class="flex-1 text-center md:text-left">
        <h2
          class="text-3xl sm:text-4xl md:text-5xl font-bold mb-4 leading-tight"
        >
          SAFE & CONVENIENT <br />
          MOBILE APP
        </h2>
        <p class="text-base sm:text-lg mb-6">
          Booking Flights, Checking Flight Status and Check-in and boarding pass
          status from Nepal Airlines Mobile Application
        </p>
        <p class="text-sm mb-3">International</p>

        <!-- Buttons -->
        <div
          class="flex flex-col sm:flex-row gap-4 justify-center md:justify-start"
        >
          <a
            href="#"
            class="bg-blue-700 hover:bg-blue-800 text-white font-medium px-6 py-2 rounded text-sm sm:text-base"
            >Play Store</a
          >
          <a
            href="#"
            class="bg-red-600 hover:bg-red-700 text-white font-medium px-6 py-2 rounded text-sm sm:text-base"
            >App Store</a
          >
        </div>
      </div>

      <!-- App Images -->
      <div class="flex gap-4 flex-wrap justify-center md:justify-end">
        <img
          src="https://via.placeholder.com/300x600"
          alt="App Screen 1"
          class="w-32 sm:w-40 md:w-56 lg:w-64 rounded-2xl shadow-lg"
        />
        <img
          src="https://via.placeholder.com/300x600"
          alt="App Screen 2"
          class="w-32 sm:w-40 md:w-56 lg:w-64 rounded-2xl shadow-lg"
        />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "MobileAppPromo",
};
</script>
