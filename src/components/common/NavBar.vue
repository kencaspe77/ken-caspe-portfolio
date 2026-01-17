<script setup>
import Links from "@/components/common/Links.vue";
</script>

<template>
  <!-- Nav bar -->
  <div class="fixed top-0 z-50 w-full flex justify-center py-4">
    <div
      class="w-[90%] max-w-7xl flex justify-between items-center px-8 py-3 bg-blue-700/40 backdrop-blur-sm text-white border border-blue-800 rounded-2xl shadow-lg"
    >
      <!-- Logo (Left) -->
      <div class="shrink-0">
        <p class="text-2xl font-bold tracking-wide">KEN</p>
      </div>
      <!-- Nav Links -->
      <Links />
    </div>
  </div>
</template>

<style scoped></style>
