<script setup>
import Button from "@/components/common/Button.vue";
import { Download } from "lucide-vue-next";
</script>

<template>
  <div
    class="relative w-full min-h-screen grid grid-cols-1 md:grid-cols-2 gap-8 overflow-hidden"
  >
    <div class="absolute inset-0 overflow-hidden pointer-events-none">
      <div
        class="absolute top-20 left-10 w-72 h-72 bg-blue-500/10 rounded-full blur-3xl"
      ></div>
      <div
        class="absolute bottom-20 right-10 w-96 h-96 bg-purple-500/10 rounded-full blur-3xl"
      ></div>
      <div
        class="absolute top-1/2 left-1/3 w-2 h-2 bg-blue-400 rounded-full animate-pulse"
      ></div>
      <div
        class="absolute top-1/3 right-1/4 w-3 h-3 bg-purple-400 rounded-full animate-pulse delay-300"
      ></div>
    </div>

    <!-- Left Content Section -->
    <div class="relative h-full pt-32 md:pt-20 col-span-1 pl-8 md:pl-20 z-10">
      <div class="h-full flex justify-end items-center">
        <div
          class="w-full md:w-5/6 flex flex-col justify-center items-start space-y-6"
        >
          <h1
            class="text-2xl md:text-3xl text-blue-300 font-light animate-fade-in"
          >
            Hey there! 👋
          </h1>
          <div class="space-y-2">
            <h1 class="text-3xl md:text-4xl font-light animate-fade-in-delay-1">
              I'm
            </h1>
            <h1 class="text-5xl md:text-7xl font-bold animate-fade-in-delay-2">
              <span
                class="bg-linear-to-r from-blue-400 via-blue-500 to-purple-500 bg-clip-text text-transparent drop-shadow-[0_0_30px_rgba(59,130,246,0.5)]"
              >
                Kengie Caspe
              </span>
            </h1>
          </div>
          <p
            class="text-xl md:text-2xl leading-relaxed text-gray-300 animate-fade-in-delay-3 max-w-xl"
          >
            A Web Developer specializing in modern frontend development with
            <span class="text-blue-400 font-semibold">Vue.js</span>,
            <span class="text-blue-400 font-semibold">Tailwind CSS</span>, and
            intuitive
            <span class="text-blue-400 font-semibold">UI/UX design</span>.
          </p>
          <div class="mt-8 animate-fade-in-delay-4">
            <Button>
              <Download :size="20" class="mr-2" />
              Download Resume
            </Button>
          </div>
        </div>
      </div>
    </div>

    <!-- Right Image Section -->
    <div class="relative col-span-1 h-full pr-8 md:pr-20 pb-10 md:pb-0 z-10">
      <div class="flex justify-center items-center h-full">
        <div class="relative group">
          <div
            class="absolute -inset-1 bg-linear-to-r from-blue-500 via-purple-500 to-blue-500 rounded-2xl blur-lg opacity-75 group-hover:opacity-100 transition duration-1000 group-hover:duration-200 animate-gradient"
          ></div>
          <div class="relative">
            <img
              class="relative border-4 border-blue-500/50 bg-gray-800/60 rounded-2xl shadow-2xl transform group-hover:scale-[1.02] transition-transform duration-500"
              src="@/assets/images/ken.png"
              alt="Ken Caspe - Web Developer"
            />
          </div>
          <div
            class="absolute -top-4 -left-4 w-8 h-8 border-t-4 border-l-4 border-blue-400 rounded-tl-lg"
          ></div>
          <div
            class="absolute -bottom-4 -right-4 w-8 h-8 border-b-4 border-r-4 border-purple-400 rounded-br-lg"
          ></div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
@keyframes fade-in {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes gradient {
  0%,
  100% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
}

.animate-fade-in {
  animation: fade-in 0.8s ease-out forwards;
}

.animate-fade-in-delay-1 {
  animation: fade-in 0.8s ease-out 0.2s forwards;
  opacity: 0;
}

.animate-fade-in-delay-2 {
  animation: fade-in 0.8s ease-out 0.4s forwards;
  opacity: 0;
}

.animate-fade-in-delay-3 {
  animation: fade-in 0.8s ease-out 0.6s forwards;
  opacity: 0;
}

.animate-fade-in-delay-4 {
  animation: fade-in 0.8s ease-out 0.8s forwards;
  opacity: 0;
}

.animate-gradient {
  background-size: 200% 200%;
  animation: gradient 3s ease infinite;
}

.delay-300 {
  animation-delay: 300ms;
}
</style>
