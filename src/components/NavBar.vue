<script setup>
import { ref } from "vue";
import { RouterLink } from "vue-router";
const isOpen = ref(false);
</script>
<template>
  <nav class="flex justify-between">
    <div class="text-3xl font-serif">Logo</div>
    <div>
      <i class="ri-menu-line text-3xl text-blue-400"></i>
    </div>
    <div class="">
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/about">About</RouterLink>
    </div>
  </nav>
</template>