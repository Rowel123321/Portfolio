<template>
  <section 
    id="about" 
    class="relative min-h-screen flex items-center bg-gray-900 text-white overflow-hidden"
  >
    <!-- Background Image -->
    <div 
      class="absolute inset-0 bg-cover bg-center opacity-20"
      style="background-image: url('https://images.unsplash.com/photo-1522071820081-009f0129c71c?auto=format&fit=crop&w=1920&q=80');"
    ></div>
    
    <!-- Overlay -->
    <div class="absolute inset-0 bg-gradient-to-r from-gray-900/90 to-gray-800/80"></div>

    <!-- Content -->
    <div class="relative w-full max-w-6xl mx-auto px-6 grid md:grid-cols-2 gap-12 items-center">
      
      <!-- Left Side: About Me -->
      <div>
        <h2 class="text-5xl font-extrabold mb-6 text-yellow-400">👨‍💻 About Me</h2>
        <p class="text-xl leading-relaxed mb-6 text-gray-200">
          Hi, I'm <span class="font-semibold text-yellow-400">Rowel  Borden </span>, 
          a passionate web developer who specializes in building elegant, responsive, 
          and user-friendly web applications.  
          I thrive on transforming ideas into functional solutions with clean, maintainable code.
        </p>
        
        <p class="text-xl leading-relaxed mb-8 text-gray-300">
          My journey in tech is driven by curiosity, creativity, and a constant desire to learn.  
          I believe great software is not just about functionality—it should also deliver meaningful 
          user experiences.
        </p>

        <!-- CTA -->
        <a href="#projects" 
           class="inline-block bg-yellow-400 text-gray-900 px-8 py-4 rounded-full font-semibold shadow-lg hover:bg-yellow-300 transition">
          View My Projects
        </a>
      </div>

      <!-- Right Side: Skills -->
      <div class="space-y-6">
        <div class="p-6 bg-white/10 rounded-2xl shadow hover:shadow-lg transition">
          <h3 class="text-2xl font-semibold text-yellow-400 mb-3">💡 Creativity</h3>
          <p class="text-lg text-gray-200">
            I enjoy solving problems with a creative approach and crafting 
            modern interfaces that feel intuitive and engaging.
          </p>
        </div>

        <div class="p-6 bg-white/10 rounded-2xl shadow hover:shadow-lg transition">
          <h3 class="text-2xl font-semibold text-yellow-400 mb-3">⚙️ Development</h3>
          <p class="text-lg text-gray-200">
            Skilled in full-stack web development, API integration, 
            and database management to deliver reliable solutions.
          </p>
        </div>

        <div class="p-6 bg-white/10 rounded-2xl shadow hover:shadow-lg transition">
          <h3 class="text-2xl font-semibold text-yellow-400 mb-3">🚀 Growth</h3>
          <p class="text-lg text-gray-200">
            Always eager to learn new technologies and adapt to the fast-changing world of software.
          </p>
        </div>
      </div>

    </div>
  </section>
</template>
