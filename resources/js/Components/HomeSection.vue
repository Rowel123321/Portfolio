<template>
  <section 
    id="home" 
    class="h-screen flex flex-col justify-center items-center text-center text-white relative overflow-hidden"
  >
    <!-- Background Image or GIF -->
    <div 
      class="absolute inset-0 bg-cover bg-center"
      style="background-image: url('https://images.unsplash.com/photo-1518770660439-4636190af475?ixlib=rb-4.0.3&auto=format&fit=crop&w=1920&q=80');"
    ></div>

    <!-- Dark Overlay -->
    <div class="absolute inset-0 bg-black/70"></div>

    <!-- Main Content -->
    <div class="relative z-10 px-6 flex flex-col items-center">
      <!-- Profile Picture -->
<img 
  src="/Images/Profile.jpg" 
  alt="Rowel Cruz" 
  class="w-40 h-40 rounded-full border-4 border-yellow-400 shadow-xl mb-6 object-cover"
/>


      <!-- Intro -->
      <h1 class="text-5xl md:text-6xl font-extrabold mb-4 drop-shadow-lg">
        Hi, I'm <span class="text-yellow-400">Rowel Borden</span> 👋
      </h1>
      <p class="text-lg md:text-2xl max-w-2xl mx-auto mb-8 text-gray-200 leading-relaxed">
        A passionate <span class="font-semibold">Web Developer</span> crafting 
        responsive, modern, and user-friendly experiences.  
        I love turning ideas into reality with creativity and clean code.
      </p>

      <!-- CTA Buttons -->
      <div class="flex flex-col sm:flex-row gap-4 justify-center">
        <a 
          href="#about" 
          class="bg-yellow-400 text-gray-900 px-8 py-3 rounded-full font-semibold shadow-lg hover:bg-yellow-300 transition"
        >
           Learn more
        </a>
        <a 
          href="#contact" 
          class="bg-white/10 border border-gray-500 px-8 py-3 rounded-full font-semibold hover:bg-white/20 transition"
        >
           Contact Me
        </a>
      </div>
    </div>
  </section>
</template>
