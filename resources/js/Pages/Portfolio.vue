<script setup>
import HomeSection from '@/Components/HomeSection.vue'
import AboutSection from '@/Components/AboutSection.vue'
import ProjectsSection from '@/Components/ProjectsSection.vue'
import ContactSection from '@/Components/ContactSection.vue'
</script>

<template>
  <div class="font-sans scroll-smooth">

    <!-- Top Navbar -->
    <nav class="fixed top-0 left-0 w-full bg-gray-900/90 backdrop-blur-md p-4 shadow-md z-50">
      <div class="max-w-5xl mx-auto flex justify-center gap-6">
        <a 
          href="#home" 
          class="px-5 py-2 rounded-full bg-white/10 hover:bg-yellow-400/20 
                 hover:text-yellow-300 transition transform hover:scale-110 
                 shadow-md hover:shadow-yellow-400/30 backdrop-blur-sm font-medium"
        >
          Home
        </a>
        <a 
          href="#about" 
          class="px-5 py-2 rounded-full bg-white/10 hover:bg-yellow-400/20 
                 hover:text-yellow-300 transition transform hover:scale-110 
                 shadow-md hover:shadow-yellow-400/30 backdrop-blur-sm font-medium"
        >
          About
        </a>
        <a 
          href="#projects" 
          class="px-5 py-2 rounded-full bg-white/10 hover:bg-yellow-400/20 
                 hover:text-yellow-300 transition transform hover:scale-110 
                 shadow-md hover:shadow-yellow-400/30 backdrop-blur-sm font-medium"
        >
          Projects
        </a>
        <a 
          href="#contact" 
          class="px-5 py-2 rounded-full bg-white/10 hover:bg-yellow-400/20 
                 hover:text-yellow-300 transition transform hover:scale-110 
                 shadow-md hover:shadow-yellow-400/30 backdrop-blur-sm font-medium"
        >
          Contact
        </a>
      </div>
    </nav>

    <!-- Sections -->
    <HomeSection />
    <AboutSection />
    <ProjectsSection />
    <ContactSection />

  </div>
</template>
