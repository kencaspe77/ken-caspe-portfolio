<script setup></script>

<template>
  <button
    class="group relative px-8 py-4 bg-linear-to-r from-blue-500 to-blue-600 text-white rounded-xl font-semibold text-lg shadow-lg hover:shadow-blue-500/50 hover:shadow-2xl transition-all duration-300 flex items-center gap-2 overflow-hidden"
  >
    <span
      class="absolute inset-0 w-full h-full bg-linear-to-r from-transparent via-white/20 to-transparent -translate-x-full group-hover:translate-x-full transition-transform duration-1000"
    ></span>

    <!-- Button content -->
    <span class="relative flex items-center gap-2">
      <slot></slot>
    </span>
  </button>
</template>

<style scoped></style>
