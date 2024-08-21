<template>
  <div class="relative flex flex-col lg:ml-[120px] lg:mr-[120px] p-2 gap-20 md:ml-[46px] md:mr-[46px] ml-[20px] ">
    <div class="absolute inset-0 z-0">
      <div class="absolute top-0 w-px h-full bg-[#E8E9EA] left-2"></div>
      <div class="absolute ml-[-200px] md:w-[955px] sm:w-[375px] lg:w-[1599px] w-[800px] h-px bg-[#E8E9EA] top-24 "></div>
    </div>

    <Navbar class="relative z-10" />

    <Content />
    <div class="absolute   w-full h-px bg-[#E8E9EA] bottom-[86px]  lg:bottom-[55px]"></div>

    <Footer />
  </div>
</template>

<script setup>
import { ref, onMounted, computed } from 'vue';

import Navbar from './components/NavBar.vue';
import Footer from './components/Footer.vue';
import Content from './components/Content.vue';
</script>



<style lang="scss" scoped>


</style>