<script setup>
import { ref } from "vue";
import { Mail, Github, Facebook } from "lucide-vue-next";

const navLinks = ref([
  { href: "#", text: "Home" },
  { href: "#about", text: "About" },
  { href: "#projects", text: "Projects" },
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
    <li v-for="link in navLinks" :key="link.text" class="group">
      <a
        :href="link.href"
        class="nav-links hover:text-purple-300 transition-colors flex items-center gap-2"
      >
        <span class="max-w-0 overflow-hidden whitespace-nowrap">
          {{ link.text }}
        </span>
      </a>
    </li>
  </ul>

  <!-- Right Social Links -->
  <ul class="flex gap-4">
    <li v-for="link in socialLinks" :key="link.href">
      <a
        :href="link.href"
        target="_blank"
        class="hover:text-purple-300 transition-colors flex items-center"
      >
        <component :is="link.icon" :size="24" />
      </a>
    </li>
  </ul>
</template>

<style scoped>
.nav-links {
  position: relative;
  display: inline-block;
}

.nav-links::after {
  content: "";
  position: absolute;
  bottom: -2px;
  left: 0;
  width: 0;
  height: 2px;
  background-color: currentColor;
  transition: width 0.3s ease-out;
}

.nav-links:hover::after {
  width: 100%;
}
</style>
