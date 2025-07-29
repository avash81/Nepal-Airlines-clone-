<template>
  <header>
    <!-- Top Header -->
    <div class="max-w-screen-xl mx-auto px-12 py-2 flex items-center">
      <!-- Logo -->
      <div>
        <img src="/logo.png" class="h-14 w-34" />
      </div>

      <!-- Right Side: Buttons + Icons -->
      <div class="flex gap-6 ml-auto">
        <!-- Buttons -->
        <div class="flex gap-2">
          <button
            class="bg-red-600 hover:bg-red-700 text-white text-sm px-3 py-1 rounded"
          >
            Online Job Application
          </button>
          <button
            class="bg-red-600 hover:bg-red-700 text-white text-sm px-3 py-1 rounded"
          >
            Manage Booking
          </button>
        </div>

        <!-- Icons -->
        <div class="flex items-center gap-4 text-gray-700 text-sm">
          <div class="flex items-center gap-1 cursor-pointer">
            <i class="fas fa-envelope"></i> Mail Login
          </div>
          <i class="fas fa-search cursor-pointer"></i>
          <div class="relative cursor-pointer">
            <i class="fas fa-bell"></i>
            <span
              class="absolute -top-1 -right-2 bg-red-600 text-white text-xs rounded-full px-1"
              >3</span
            >
          </div>
        </div>
      </div>
    </div>

    <!-- Bottom Navigation -->
    <nav class="bg-gradient-to-r from-blue-900 to-blue-500 text-white">
      <div class="max-w-screen-xl mx-auto px-12 py-6 flex items-center">
        <ul class="flex flex-wrap gap-16 text-sm">
          <li class="cursor-pointer hover:text-[#76b1f3]">Booking</li>
          <li class="cursor-pointer hover:text-[#76b1f3]">Services</li>
          <li class="cursor-pointer hover:text-[#76b1f3]">Schedule</li>
          <li class="cursor-pointer hover:text-[#76b1f3]">Destinations</li>
          <li class="cursor-pointer hover:text-[#76b1f3]">
            Boarding Pass Privileges
          </li>
          <li class="cursor-pointer hover:text-[#76b1f3]">Publication</li>
          <li class="cursor-pointer hover:text-[#76b1f3]">Notices</li>
          <li class="cursor-pointer hover:text-[#76b1f3]">Contact</li>
        </ul>
      </div>
    </nav>
  </header>
</template>
<script setup></script>
