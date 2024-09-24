<script setup>
import MyButton from "../components/ButtonComponent.vue"; // Assure-toi que le chemin est correct
</script>

<template>
  <main>
    <div class="m-auto">
      <h1>Hello !</h1>
    </div>
    <div class="flex space-x-5">
      <MyButton type="primary">
        button 1
      </MyButton>
      <MyButton type="danger">
        button 2
      </MyButton>
      <MyButton type="secondary">
        button 3
      </MyButton>
      <MyButton type="secondary" isDisabled>
        button 3
      </MyButton>
    </div>
  </main>
</template>
