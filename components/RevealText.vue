<template>
    <div class="flex flex-row my-2">
      <div class="basis-5/12 md:basis-2/12 my-auto">{{ label }}: </div>
      <div class="basis-full bg-gray-800 p-2" v-if="show">{{ value }}</div>
      <div class="basis-full bg-gray-800 p-2 text-center" style="cursor: pointer" v-else @click="toggleShow">click to reveal</div>
    </div>
  </template>
  
  <script setup lang="ts">
  import { ref, defineProps } from 'vue';
  
  // Define the props the component accepts
  const props = defineProps<{
    label: string;
    value: string;
  }>();
  
  // Convert `show` prop to a reactive ref that can be toggled
  const show = ref(false);
  
  // Method to toggle the visibility
  function toggleShow() {
    show.value = true;
  }
  </script>
  