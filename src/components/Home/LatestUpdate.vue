<template>
  <section class="max-w-screen-xl mx-auto px-4 md:px-12 py-8">
    <!-- Header -->
    <div class="flex justify-between items-center mb-6">
      <h2 class="text-2xl font-bold text-blue-800 uppercase">Latest Updates</h2>
      <a
        href="https://nepalairlines.com.np/news"
        class="text-red-600 hover:underline text-sm"
        >+ View All</a
      >
    </div>

    <!-- Grid Layout -->
    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
      <!-- Update Card -->
      <div
        v-for="(item, index) in updates"
        :key="index"
        class="bg-white shadow-md rounded-lg overflow-hidden flex flex-col md:flex-row"
      >
        <!-- Image -->
        <div v-if="item.image" class="md:w-1/3">
          <img :src="item.image" alt="" class="w-full h-full object-cover" />
        </div>

        <!-- Content -->
        <div class="flex-1 p-4 relative">
          <!-- Date Badge -->
          <div
            class="absolute top-0 left-0 bg-red-600 text-white px-3 py-1 text-center"
          >
            <p class="text-lg font-bold leading-none">{{ item.date.day }}</p>
            <p class="text-xs uppercase">{{ item.date.month }}</p>
          </div>

          <div class="pl-16">
            <h3 class="text-gray-800 font-medium text-lg">
              {{ item.title }}
            </h3>
            <p v-if="item.description" class="text-gray-600 text-sm mt-2">
              {{ item.description }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "LatestUpdates",
  data() {
    return {
      updates: [
        {
          date: { day: "03", month: "May" },
          title: "Press Note: Meeting With President of Nepal",
          image: "/Home/President.png", // Replace with your image
        },
        {
          date: { day: "09", month: "Feb" },
          title:
            "Notice for Check-in counter opening hours of KTM-DXB and KTM-DMM",
          image: "/Home/Nepal_airlines.png", // Replace with airline logo
        },
        {
          date: { day: "12", month: "Sep" },
          title: "Notice for Passengers travelling from Bengaluru to KTM",
          image: "/Home/Notice.png",
        },
      ],
    };
  },
};
</script>

<style scoped>
/* Date Badge positioning */
</style>
