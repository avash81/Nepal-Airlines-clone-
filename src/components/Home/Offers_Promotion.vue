<template>
  <section>
    <div class="max-w-screen-xl mx-auto px-4 md:px-12 py-8">
      <!-- Header -->
      <div class="flex mb-6 items-center">
        <h2 class="text-[#003594] text-lg md:text-3xl">OFFERS & PROMOTION</h2>
        <div class="ml-auto text-sm sm:text-md md:text-xl">
          <a href="https://nepalairlines.com.np/offers" class="text-[#C51D34]">
            + View All
          </a>
        </div>
      </div>

      <!-- Carousel Container -->
      <div
        class="relative w-full flex items-center justify-center group overflow-hidden"
      >
        <!-- Slide Cards -->
        <div
          class="flex gap-4 sm:gap-6 transition-transform duration-500"
          :style="{
            transform: `translateX(-${startIndex * (100 / cardsPerView)}%)`,
            width: `${(images.length * 100) / cardsPerView}%`,
          }"
        >
          <div
            v-for="(img, index) in images"
            :key="index"
            class="w-full sm:w-1/2 lg:w-1/3 px-1 flex-shrink-0"
          >
            <div
              class="sm:h-[180px] md:h-[300px] mx-auto border rounded-lg shadow-md bg-white"
            >
              <a :href="links[index]">
                <img
                  :src="img"
                  class="object-cover w-full h-48 sm:h-56 rounded-t-md"
                  alt=""
                />
                <p
                  class="px-4 py-2 text-sm sm:text-base md:text-xl text-[#C51D34]"
                >
                  {{ headings[index] }}
                </p>
              </a>
            </div>
          </div>
        </div>

        <!-- Left Arrow -->
        <button
          v-if="startIndex > 0"
          @click="prevSlide"
          class="absolute left-2 top-1/2 transform -translate-y-1/2 bg-white/80 hover:bg-white text-black rounded-full text-xl sm:text-2xl opacity-0 group-hover:opacity-100 transition-opacity duration-300 px-2 sm:px-3 z-10"
        >
          ❮
        </button>

        <!-- Right Arrow -->
        <button
          v-if="startIndex + cardsPerView < images.length"
          @click="nextSlide"
          class="absolute right-2 top-1/2 transform -translate-y-1/2 bg-white/80 hover:bg-white text-black rounded-full text-xl sm:text-2xl opacity-0 group-hover:opacity-100 transition-opacity duration-300 px-2 sm:px-3 z-10"
        >
          ❯
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, computed, onMounted, onUnmounted } from "vue";

// Data
const images = [
  "/Home/Fly_Nepal_Airlines.png",
  "/Home/Excess_Badges.png",
  "/Home/Employee_And_Family_Member.png",
  "/Home/Boarding_pass.png",
];

const headings = [
  "Fly Nepal Airlines",
  "Excess Badges? No Worries",
  "Employee And Family Member",
  "Boarding Pass Offer",
];

const links = images.map(() => "https://nepalairlines.com.np/offers");

// Reactive values
const startIndex = ref(0);
const cardsPerView = ref(3);

// Responsive logic
function updateCardsPerView() {
  const width = window.innerWidth;
  if (width < 640) {
    cardsPerView.value = 1;
  } else if (width < 1024) {
    cardsPerView.value = 2;
  } else {
    cardsPerView.value = 3;
  }
}

// Slide controls
function nextSlide() {
  if (startIndex.value + cardsPerView.value < images.length) {
    startIndex.value++;
  }
}
function prevSlide() {
  if (startIndex.value > 0) {
    startIndex.value--;
  }
}

// Lifecycle hooks
onMounted(() => {
  updateCardsPerView();
  window.addEventListener("resize", updateCardsPerView);
});
onUnmounted(() => {
  window.removeEventListener("resize", updateCardsPerView);
});
</script>
