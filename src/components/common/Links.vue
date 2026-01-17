<script setup>
import { ref } from "vue";
import { Mail, Github, Facebook } from "lucide-vue-next";
const navLinks = ref([
  { href: "#", text: "Home" },
  { href: "#projects", text: "Projects" },
  { href: "#about", text: "About" },
  { href: "#resume", text: "Resume" },
]);

const socialLinks = ref([
  { href: "https://github.com/kencaspe77", icon: Github },
  { href: "https://www.facebook.com/kengie.tan.caspe/", icon: Facebook },
  { href: "mailto:kencaspe77@gmail.com", icon: Mail },
]);
</script>
<template>
  <!-- Center Navigation Links -->
  <ul class="flex gap-10">
    <li v-for="link in navLinks" :key="link.text">
      <a
        :href="link.href"
        class="hover:text-sky-500 transition-colors flex items-center gap-2"
      >
        <component :is="link.icon" :size="20" />
        <span class="">{{ link.text }}</span>
      </a>
    </li>
  </ul>
  <!-- Right Social Links -->
  <ul class="flex gap-4">
    <li v-for="link in socialLinks" :key="link.href">
      <a
        :href="link.href"
        class="hover:text-sky-500 transition-colors flex items-center"
      >
        <component :is="link.icon" :size="24" />
      </a>
    </li>
  </ul>
</template>
<style scoped></style>
