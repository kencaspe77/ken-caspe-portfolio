<script setup>
import Links from "@/components/common/Links.vue";
</script>

<template>
  <!-- Nav bar -->
  <div class="fixed top-0 z-50 w-full flex justify-center py-4">
    <div
      class="w-[90%] max-w-7xl flex justify-between items-center px-8 py-3 backdrop-blur-md text-white rounded-2xl shadow-2xl bg-linear-to-r from-slate-900/90 via-blue-900/90 to-slate-900/90 border border-blue-500/30"
    >
      <!-- Logo (Left) -->
      <div class="shrink-0">
        <p class="text-2xl font-bold tracking-wide">KEN CASPE</p>
      </div>
      <!-- Nav Links -->
      <Links />
    </div>
  </div>
</template>

<style scoped></style>
