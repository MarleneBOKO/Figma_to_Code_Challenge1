<template>
  <div class="flex flex-row items-center justify-between p-2">
    <div>
      <img src="/public/Images/Frame (1).png" alt="">
    </div>

    <!-- Menu Burger -->
    <div class="lg:hidden relative z-50">
      <button @click="toggleMenu" class="text-[#12171F] focus:outline-none">
        <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 20 20" fill="none">
          <path d="M2.65 6C2.65 5.25442 3.25442 4.65 4 4.65H17C17.7456 4.65 18.35 5.25442 18.35 6V7C18.35 7.74558 17.7456 8.35 17 8.35H4C3.25442 8.35 2.65 7.74558 2.65 7V6ZM2.65 13C2.65 12.2544 3.25442 11.65 4 11.65H17C17.7456 11.65 18.35 12.2544 18.35 13V14C18.35 14.7456 17.7456 15.35 17 15.35H4C3.25442 15.35 2.65 14.7456 2.65 14V13Z" stroke="#0B0D12" stroke-width="1.3"/>
        </svg>
      </button>
    </div>

    <!-- Navbar Links -->
    <div :class="{'hidden lg:flex flex-row gap-7': true}">
      <ul class="flex flex-row gap-7">
        <li class="text-base font-semibold text-[#12171F]">Home</li>
        <li class="text-base font-semibold text-[#12171F]">Top sales</li>
        <li class="text-base font-semibold text-[#12171F]">Collections</li>
        <li class="text-base font-semibold text-[#12171F]">Our blog</li>
        <li class="text-base font-semibold text-[#12171F]">About us</li>
      </ul>
    </div>

    <!-- Sign up and Connect Wallet -->
    <div class="hidden lg:flex flex-row items-center justify-between gap-5">
      <a href="#" class="text-[#0E1218] text-[16px] font-semibold">Sign up</a>
      <hr class="w-8 font-bold rounded rotate-90 bg-[#0E1218]">
      <button class="bg-[#0E1218] text-white flex items-center font-semibold justify-center w-[170px] h-[44px] text-[16px] rounded-[42px]">Connect Wallet</button>
    </div>
  </div>

  <!-- Menu Dropdown for Mobile -->
  <div v-if="isMenuOpen" class="flex flex-col mt-4 gap-7 lg:hidden">
    <div class="flex justify-end">
      <div @click="isMenuOpen" class="flex items-center justify-center w-[30px] h-[30px] rounded-lg p-2 bg-[#E8E9EA]">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
          <path stroke-linecap="round" stroke-linejoin="round" d="M6 18 18 6M6 6l12 12" />
        </svg>
      </div>
    </div>
    <ul class="flex flex-col gap-4">
      <li class="text-base font-semibold text-[#12171F]">Home</li>
      <li class="text-base font-semibold text-[#12171F]">Top sales</li>
      <li class="text-base font-semibold text-[#12171F]">Collections</li>
      <li class="text-base font-semibold text-[#12171F]">Our blog</li>
      <li class="text-base font-semibold text-[#12171F]">About us</li>
    </ul>
    <div class="flex items-center justify-center gap-5">
      <a href="#" class="text-[#0E1218] text-[16px] font-semibold">Sign up</a>
      <hr class="w-8 font-bold rounded rotate-90 bg-[#0E1218]">
      <button class="bg-[#0E1218] text-white flex items-center font-semibold justify-center w-[170px] h-[44px] text-[16px] rounded-[42px]">Connect Wallet</button>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const isMenuOpen = ref(false);

function toggleMenu() {
  isMenuOpen.value = !isMenuOpen.value;
}
</script>

<style lang="scss" scoped>
/* Add your styles here */
</style>
