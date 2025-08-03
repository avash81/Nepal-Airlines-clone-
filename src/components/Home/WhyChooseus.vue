<template>
  <section class="py-12 sm:py-16 bg-white">
    <!-- Top Banner -->
    <div
      class="relative flex justify-center items-center bg-red-700 text-white p-6 sm:p-8 lg:p-10 mb-12 max-w-6xl mx-auto rounded-lg overflow-hidden"
    >
      <div
        class="flex flex-col md:flex-row md:items-center md:justify-between w-full gap-6"
      >
        <!-- Text -->
        <div>
          <h2 class="text-2xl sm:text-3xl md:text-4xl font-bold leading-tight">
            Flying Above and <br />Beyond
          </h2>
          <a
            href="#"
            class="inline-block mt-4 border border-white px-6 py-2 rounded hover:bg-white hover:text-red-700 transition text-sm sm:text-base"
          >
            Explore Destinations
          </a>
        </div>

        <!-- Airplane Image -->
        <img
          src="/Home/Aepal_a.png"
          alt="Airplane"
          class="w-40 sm:w-52 md:w-60 lg:w-72 mt-4 md:mt-0 md:ml-8 rounded-lg object-cover"
        />
      </div>
    </div>

    <!-- Section Title -->
    <h2
      class="text-2xl sm:text-3xl text-center text-blue-800 font-bold mb-10 sm:mb-12"
    >
      WHY CHOOSE US
    </h2>

    <!-- Cards Grid -->
    <div
      class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6 px-4 sm:px-6 lg:px-20"
    >
      <div
        v-for="(item, index) in reasons"
        :key="index"
        class="bg-white shadow-md rounded-lg p-6 text-center border border-gray-100 hover:shadow-lg transition"
      >
        <div
          class="w-14 h-14 sm:w-16 sm:h-16 mx-auto mb-4 flex items-center justify-center border border-red-300 rounded-full"
        >
          <span class="text-2xl sm:text-3xl text-red-600">{{ item.icon }}</span>
        </div>
        <h3 class="text-lg sm:text-xl font-semibold text-red-600 mb-2">
          {{ item.title }}
        </h3>
        <p class="text-gray-600 text-sm sm:text-base">
          {{ item.description }}
        </p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "WhyChooseUs",
  data() {
    return {
      reasons: [
        {
          icon: "🏢",
          title: "Experience",
          description: "We have been providing excellent service over 60 years",
        },
        {
          icon: "😊",
          title: "Happy Passengers",
          description: "Our passengers are very happy with our service.",
        },
        {
          icon: "👍",
          title: "Outstanding Services",
          description: "We have been providing outstanding services till date",
        },
        {
          icon: "💵",
          title: "Competitive Fare",
          description: "Our fare is competitive as compared to other airlines",
        },
      ],
    };
  },
};
</script>
