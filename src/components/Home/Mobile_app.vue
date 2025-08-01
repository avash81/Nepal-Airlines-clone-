<template>
  <section
    class="relative w-full bg-cover bg-center text-white"
    style="background-image: url('/Home/Fly_Nepal_Airlines.png')"
  >
    <div class="absolute inset-0 bg-black bg-opacity-50"></div>

    <div
      class="relative container mx-auto px-6 lg:px-20 py-20 flex flex-col md:flex-row items-center md:items-start gap-10"
    >
      <!-- Text Content -->
      <div class="flex-1">
        <h2 class="text-4xl md:text-5xl font-bold mb-4 leading-tight">
          SAFE & CONVENIENT <br />
          MOBILE APP
        </h2>
        <p class="text-lg mb-6">
          Booking Flights, Checking Flight Status and Check-in and boarding pass
          status from Nepal Airlines Mobile Application
        </p>
        <p class="text-sm mb-2">International</p>

        <!-- Buttons -->
        <div class="flex gap-4">
          <a
            href="#"
            class="bg-blue-700 hover:bg-blue-800 text-white font-medium px-6 py-2 rounded"
            >Play Store</a
          >
          <a
            href="#"
            class="bg-red-600 hover:bg-red-700 text-white font-medium px-6 py-2 rounded"
            >App Store</a
          >
        </div>
      </div>

      <!-- Mobile Images -->
      <div class="flex gap-6 justify-center md:justify-end">
        <img
          src="https://via.placeholder.com/300x600"
          alt="App Screen 1"
          class="w-40 md:w-64 rounded-2xl shadow-lg"
        />
        <img
          src="https://via.placeholder.com/300x600"
          alt="App Screen 2"
          class="w-40 md:w-64 rounded-2xl shadow-lg"
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
