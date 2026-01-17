<script setup>
import NavBar from "@/components/common/NavBar.vue";
import Hero from "@/components/sections/Hero.vue";
import Projects from "@/components/sections/Projects.vue";
import About from "@/components/sections/About.vue";
import Resume from "@/components/sections/Resume.vue";
import Footer from "@/components/common/Footer.vue";

const sections = [
  {
    id: "home",
    component: Hero,
    bgColor: "bg-amber-950",
    textColor: "text-white",
  },
  {
    id: "projects",
    component: Projects,
    bgColor: "bg-blue-950",
    textColor: "text-white",
  },
  {
    id: "about",
    component: About,
    bgColor: "bg-red-950",
    textColor: "text-white",
  },
  {
    id: "resume",
    component: Resume,
    bgColor: "bg-yellow-950",
    textColor: "text-white",
  },
];
</script>
<template>
  <div class="h-screen">
    <header>
      <NavBar />
    </header>
    <!-- Home View Content -->
    <main>
      <section
        v-for="section in sections"
        :key="section.id"
        :id="section.id"
        :class="[
          'h-screen flex flex-col justify-center items-center',
          section.bgColor,
          section.textColor,
        ]"
      >
        <component :is="section.component" />
      </section>
    </main>
    <footer class="bg-slate-900 border-t border-slate-800 py-12">
      <Footer />
    </footer>
  </div>
</template>
<style scoped></style>
