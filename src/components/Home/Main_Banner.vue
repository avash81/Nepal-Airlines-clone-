<template>
  <section class="relative w-full h-[500px] overflow-hidden group">
    <!-- Background Image -->
    <img
      :src="images[currentIndex]"
      alt="City Image"
      class="w-full h-full object-cover transition duration-500"
    />

    <!-- Overlay Content -->
    <div
      class="absolute inset-0 flex flex-col items-center justify-center text-white px-12"
    >
      <Transition name="fade-slide" mode="out-in">
        <h2
          :key="'heading-' + currentIndex"
          class="text-3xl md:text-5xl font-bold mb-4"
        >
          {{ headings[currentIndex] }}
        </h2>
      </Transition>

      <Transition name="fade-slide" mode="out-in">
        <button
          :key="'button-' + currentIndex"
          class="border border-white px-4 py-2 mb-6 hover:bg-white hover:text-black transition"
        >
          READ MORE
        </button>
      </Transition>

      <Transition name="fade-slide" mode="out-in">
        <div :key="'buttons-' + currentIndex" class="flex gap-4">
          <button
            class="bg-red-700 px-6 py-2 rounded text-white font-semibold hover:bg-red-800"
          >
            International Booking
          </button>
          <button
            class="bg-blue-700 px-6 py-2 rounded text-white font-semibold hover:bg-blue-800"
          >
            Domestic Booking
          </button>
        </div>
      </Transition>
    </div>

    <!-- Left Arrow -->
    <button
      @click="prevSlide"
      class="absolute top-1/2 left-4 transform -translate-y-1/2 text-white p-4 rounded-full text-3xl opacity-0 group-hover:opacity-100 transition-opacity duration-300 z-20"
    >
      ❮
    </button>

    <!-- Right Arrow -->
    <button
      @click="nextSlide"
      class="absolute top-1/2 right-4 transform -translate-y-1/2 text-white p-4 rounded-full text-3xl opacity-0 group-hover:opacity-100 transition-opacity duration-300 z-20"
    >
      ❯
    </button>

    <!-- -->
  </section>
</template>

<script setup>
import { ref } from "vue";

// Carousel data
const images = ["/Home/Dubai.png", "/Home/Bangkok.png", "/Home/Singapore.png"];

const headings = [
  "KATHMANDU TO DUBAI",
  "KATHMANDU TO BANGKOK",
  "KATHMANDU TO SINGAPORE",
];

const currentIndex = ref(0);

// Navigation
function nextSlide() {
  currentIndex.value = (currentIndex.value + 1) % images.length;
}

function prevSlide() {
  currentIndex.value = (currentIndex.value - 1 + images.length) % images.length;
}
</script>

<style scoped>
.fade-slide-enter-active,
.fade-slide-leave-active {
  transition: all 0.6s ease;
}
.fade-slide-enter-from {
  opacity: 0;
  transform: translateY(20px);
}
.fade-slide-leave-to {
  opacity: 0;
  transform: translateY(-10px);
}
</style>
