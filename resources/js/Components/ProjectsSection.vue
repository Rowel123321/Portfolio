<script setup>
import { ref } from 'vue'

// Projects data WITH individual expanded flag
const projects = ref([
{
  id: 1,
  name: "Libratek",
  image: "/Images/Profile.jpg",
  description: "An IoT-powered library management system that uses RFID and microcontrollers to track books in real time. When a book is borrowed, the system automatically updates its status on the website as unavailable. If a book is missing or unreturned, it is flagged in the system. An additional RFID reader at the exit monitors unauthorized removals, instantly notifying the system when a book is taken outside without proper checkout.",
  technologies: ["PHP (Native)", "JavaScript", "CSS", "C++", "Microcontroller", "RFID"],
  expanded: false,
},
{
  id: 2,
  name: "RRCY",
  image: "/Images/Profile.jpg",
  description: "A complete digital case management and operations system developed for the Regional Rehabilitation Center for Youth (RRCY). The platform manages child records, intake details, progress reports, and case histories while also handling inventories, monthly checklists, and activity monitoring. It replaces manual paperwork with a fully digital workflow, improving efficiency, accuracy, and accessibility for staff. Built with Laravel, Vue.js, and Tailwind CSS, the system provides a modern, secure, and user-friendly interface tailored for institutional needs.",
  technologies: ["Laravel", "Vue.js", "JavaScript", "Tailwind CSS"],
  expanded: false,
},
{
  id: 3,
  name: "EduScan",
  image: "/Images/Profile.jpg",
  description: "An IoT-powered classroom interactivity system that leverages RFID and microcontrollers to make learning more engaging. Students participate in multiple-choice activities by simply tapping their RFID cards on a reader, which instantly records their responses and updates the system in real time. The platform promotes active participation, reduces manual checking, and provides teachers with immediate insights into student understanding. Designed for scalability, EduScan demonstrates how IoT can transform traditional classrooms into smart, interactive learning environments.",
  technologies: ["PHP (Native)", "JavaScript", "CSS", "C++", "Microcontroller", "RFID"],
  expanded: false,
},
])

// Toggle ONLY that project
const toggleExpand = (project) => {
  project.expanded = !project.expanded
}

// Assign color per technology
const techColor = (tech) => {
  const colors = {
    "PHP (Native)": "bg-purple-500 text-white",
    "JavaScript": "bg-yellow-400 text-black",
    "CSS": "bg-blue-500 text-white",
    "C++": "bg-indigo-600 text-white",
    "Microcontroller": "bg-green-500 text-white",
    "RFID": "bg-red-400 text-white",
    "Laravel": "bg-red-600 text-white",
    "Vue.js": "bg-green-400 text-black",
    "Tailwind CSS": "bg-teal-400 text-white", // 👈 Tailwind badge color
  }
  return colors[tech] || "bg-gray-300 text-gray-800"
}
</script>

<template>
  <section id="projects" class="relative min-h-screen py-20 text-center text-white overflow-hidden">
    <!-- Background Image -->
    <div 
      class="absolute inset-0 bg-fixed bg-cover bg-center"
style="background-image: url('https://images.unsplash.com/photo-1505685296765-3a2736de412f?auto=format&fit=crop&w=1920&q=80');"


    ></div>

    <!-- Dark Overlay -->
    <div class="absolute inset-0 bg-gradient-to-r from-black/95 via-gray-900/90 to-black/85"></div>

    <!-- Content -->
    <div class="relative max-w-6xl mx-auto px-6">
      <h2 class="text-5xl font-extrabold mb-12 text-yellow-400 drop-shadow-lg">
        🚀 My Projects
      </h2>

      <!-- Cards Container (Centered) -->
      <div class="flex flex-wrap justify-center gap-10">
        <div 
          v-for="project in projects" 
          :key="project.id" 
          class="w-full md:w-1/3 flex flex-col rounded-2xl shadow-xl overflow-hidden 
                 bg-white/10 backdrop-blur-md border border-white/20 
                 transform transition duration-300 hover:scale-105 hover:shadow-yellow-400/50 hover:border-yellow-400/50"
        >
          <!-- Project Image -->
          <img 
            :src="project.image" 
            :alt="project.name" 
            class="w-full h-48 object-cover hover:opacity-90 transition cursor-pointer"
            @click="toggleExpand(project)"
          />

          <!-- Project Content -->
          <div class="p-6 flex flex-col">
            <!-- Title -->
            <h3 
              class="text-2xl font-bold text-yellow-400 hover:text-yellow-300 transition mb-4 cursor-pointer"
              @click="toggleExpand(project)"
            >
              {{ project.name }}
            </h3>

            <!-- Technologies (colored bubbles) -->
            <div class="flex flex-wrap gap-2 mb-4 justify-center md:justify-start">
              <span 
                v-for="tech in project.technologies" 
                :key="tech"
                class="px-2 py-0.5 text-xs font-medium rounded shadow-md transition transform hover:scale-105 cursor-default"
                :class="techColor(tech)"
              >
                {{ tech }}
              </span>
            </div>

            <!-- Expandable Description -->
            <transition name="expand-fade">
              <p 
                v-if="project.expanded" 
                class="mt-2 text-gray-200 leading-relaxed text-sm text-justify"
              >
                {{ project.description }}
              </p>
            </transition>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>


<style scoped>
.expand-fade-enter-active,
.expand-fade-leave-active {
  transition: all 0.3s ease;
  overflow: hidden;
}
.expand-fade-enter-from,
.expand-fade-leave-to {
  opacity: 0;
  max-height: 0;
  transform: translateY(-10px);
}
.expand-fade-enter-to,
.expand-fade-leave-from {
  opacity: 1;
  max-height: 500px; /* enough for text */
  transform: translateY(0);
}
</style>
