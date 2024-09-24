<script setup>
import MyButton from "../components/ButtonComponent.vue";
import TitreNiv1 from "../components/TitreNiv1.vue";
</script>

<template>
  <main>
    <div class="m-auto">
      <TitreNiv1>Hello !</TitreNiv1>
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
