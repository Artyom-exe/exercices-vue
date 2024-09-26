<script setup>
import { ref } from "vue";
import { RouterLink } from "vue-router";

const isOpen = ref(false);

const toggleMenu = () => {
  isOpen.value = !isOpen.value;
};
</script>
<template>
  <nav class="flex justify-between items-center">
    <div class="text-3xl font-serif">Logo</div>
    
    <!-- Icone du menu -->

    <i 
      class="ri-menu-line text-3xl text-blue-400 md:hidden cursor-pointer" 
      :class="isOpen ? 'ri-close-large-line' : 'ri-menu-line'" 
      @click="toggleMenu"
    ></i>
    
    <!-- Liens du menu (affichés sur grands écrans, masqués sur petits) -->
    <div class="hidden sm:flex space-x-4">
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/about">About</RouterLink>
      <RouterLink to="/contact">Contact</RouterLink>
    </div>

    <!-- Menu déroulant sur mobile (affiché si isOpen est true) -->
    <div 
      v-if="isOpen" 
      class="absolute top-9 left-0 w-full bg-white shadow-md md:hidden flex flex-col items-center space-y-4 p-4"
    >
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/about">About</RouterLink>
      <RouterLink to="/contact">Contact</RouterLink>
    </div>
  </nav>
</template>
