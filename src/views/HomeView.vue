<script setup>
import NavBar from "@/components/common/NavBar.vue";
import Hero from "@/components/sections/Hero.vue";
import Skills from "@/components/sections/Skills.vue";
import Projects from "@/components/sections/Projects.vue";
import About from "@/components/sections/About.vue";
import Footer from "@/components/common/Footer.vue";

const sections = [
  {
    id: "home",
    component: Hero,
  },
  {
    id: "skills",
    component: Skills,
  },
  {
    id: "about",
    component: About,
  },
  {
    id: "projects",
    component: Projects,
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
        class="h-screen flex flex-col justify-center items-center bg-linear-to-r from-slate-900/90 via-blue-900/90 to-slate-900/90"
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
