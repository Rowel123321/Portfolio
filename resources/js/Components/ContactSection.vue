<template>
  <section
    id="contact"
    class="relative min-h-screen flex items-center justify-center text-white overflow-hidden"
  >
    <!-- Background Image -->
    <div
      class="absolute inset-0 bg-cover bg-center"
      style="background-image: url('https://images.unsplash.com/photo-1531482615713-2afd69097998?auto=format&fit=crop&w=1920&q=80');"
    ></div>

    <!-- Dark Overlay -->
    <div class="absolute inset-0 bg-gradient-to-r from-black/90 via-gray-900/85 to-black/80"></div>

    <!-- Content -->
    <div class="relative max-w-4xl w-full px-6 py-12 text-center">
      <!-- Heading -->
      <h2 class="text-5xl font-extrabold mb-6 text-yellow-400 drop-shadow-lg">
        📬 Get in Touch
      </h2>
      <p class="text-lg mb-10 text-gray-300">
        I’d love to hear from you! Whether it’s a project, collaboration, or just a friendly hello.
      </p>

      <!-- Contact Info -->
      <div class="flex flex-col md:flex-row justify-center gap-12 mb-12">
        <div class="flex flex-col items-center">
          <span class="text-3xl">📧</span>
          <a
            href="mailto:rantonioborden@gmail.com"
            class="mt-2 hover:underline text-lg text-gray-200"
          >
            rantonioborden@gmail.com
          </a>
        </div>
        <div class="flex flex-col items-center">
          <span class="text-3xl">📱</span>
          <a
            href="tel:+639303927715"
            class="mt-2 hover:underline text-lg text-gray-200"
          >
            0930-392-7715
          </a>
        </div>
      </div>

      <!-- Contact Form -->
      <form
        class="bg-black/40 backdrop-blur-md p-8 rounded-2xl shadow-2xl max-w-2xl mx-auto border border-white/10"
      >
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
          <input
            type="text"
            placeholder="Your Name"
            class="w-full p-3 rounded-lg bg-white/10 text-white placeholder-gray-400 focus:ring-2 focus:ring-yellow-400 outline-none"
          />
          <input
            type="email"
            placeholder="Your Email"
            class="w-full p-3 rounded-lg bg-white/10 text-white placeholder-gray-400 focus:ring-2 focus:ring-yellow-400 outline-none"
          />
        </div>
        <textarea
          placeholder="Your Message"
          rows="5"
          class="w-full p-3 rounded-lg bg-white/10 text-white placeholder-gray-400 focus:ring-2 focus:ring-yellow-400 outline-none mb-6"
        ></textarea>
        <button
          type="submit"
          class="w-full bg-yellow-400 text-gray-900 font-bold py-3 rounded-lg hover:bg-yellow-300 transition shadow-lg"
        >
          🚀 Send Message
        </button>
      </form>
    </div>
  </section>
</template>
