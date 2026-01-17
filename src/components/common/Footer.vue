<script setup>
import { Github, Facebook, Mail, MapPin } from "lucide-vue-next";
import { ref } from "vue";

const currentYear = ref(new Date().getFullYear());

const quickLinks = ref([
  { label: "Home", href: "#" },
  { label: "About", href: "#about" },
  { label: "Projects", href: "#projects" },
  { label: "Resume", href: "#resume" },
]);

const socialLinks = ref([
  { icon: Github, href: "https://github.com/kencaspe77", label: "GitHub" },
  {
    icon: Facebook,
    href: "https://www.facebook.com/kengie.tan.caspe/",
    label: "Facebook",
  },
  { icon: Mail, href: "mailto:kencaspe77@gmail.com", label: "Email" },
]);
</script>
<template>
  <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
    <!-- Main Footer Content -->
    <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-8">
      <!-- About Section -->
      <div>
        <h3 class="text-xl font-bold text-white mb-4">Ken Caspe</h3>
        <p class="text-slate-400 text-sm leading-relaxed">
          Full-stack developer crafting beautiful and functional web
          experiences.
        </p>
        <div class="flex items-center gap-2 text-slate-400 text-sm mt-3">
          <MapPin :size="16" />
          <span>Philippines</span>
        </div>
      </div>

      <!-- Quick Links -->
      <div>
        <h4 class="text-white font-semibold mb-4">Quick Links</h4>
        <ul class="space-y-2">
          <li v-for="link in quickLinks" :key="link.label">
            <a
              :href="link.href"
              class="text-slate-400 hover:text-sky-500 transition-colors duration-300 text-sm"
            >
              {{ link.label }}
            </a>
          </li>
        </ul>
      </div>

      <!-- Social Links -->
      <div>
        <h4 class="text-white font-semibold mb-4">Connect</h4>
        <div class="flex gap-4">
          <a
            v-for="social in socialLinks"
            :key="social.label"
            :href="social.href"
            :title="social.label"
            class="text-slate-400 hover:text-sky-500 transition-colors duration-300"
          >
            <component :is="social.icon" :size="24" />
          </a>
        </div>
      </div>
    </div>

    <!-- Divider -->
    <div class="border-t border-slate-800 my-8"></div>

    <!-- Bottom Footer -->
    <div class="flex flex-col sm:flex-row justify-between items-center gap-4">
      <p class="text-slate-500 text-sm">
        &copy; {{ currentYear }} Ken Caspe. All rights reserved.
      </p>
      <p class="text-slate-500 text-sm">
        Designed & Built with ❤️ using Vue & Vite
      </p>
    </div>
  </div>
</template>
<style scoped>
footer {
  background: linear-gradient(
    135deg,
    rgba(15, 23, 42, 0.95) 0%,
    rgba(30, 41, 59, 0.95) 100%
  );
}
</style>
