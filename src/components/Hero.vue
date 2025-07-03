<script setup lang="ts">
const stats = ref([
  { value: '+2500', label: 'Happy Clients' },
  { value: '+1200', label: 'Projects Completed' },
  { value: '+1500', label: 'Cups of Coffee'},
  { value: '+10', label: 'Awards Won'}
])
</script>

<template>
    <header class="relative overflow-hidden bg-gradient-to-r from-pink-100 to-purple-100" id="#home">
      <article class="max-w-screen-xl mx-auto px-4 sm:px-8 py-16 md:py-28 flex flex-col-reverse
      lg:flex-row items-center gap-10 lg:gap-20">
        <section class="w-full lg:w-1/2 text-center lg:text-left">
          <hgroup data-aos="fade-up" data-aos-duration="500">
            <h1 class="text-3xl sm:text-4xl md:text-5xl lg:text-6xl font-bold text-gray-800 mb-4">
              Enhance your natural
            <mark class="text-pink-600 bg-transparent">Beauty</mark>
            </h1>
            <p class="text-base sm:text-lg md:text-xl text-gray-600 mb-8 max-w-xl mx-auto lg:mx-0">
              Takéo Province is located in the southwestern part of the Kingdom of Cambodia.
              The provincial capital is Daun Keo City, 77 kilometers by National Road 2 and 87
              kilometers by National Road 3.
            </p>
          </hgroup>
          <nav data-aos="fade-up" data-aos-duration="600">
            <a href="#appointment" class="bg-pink-600 hover:bg-pink-700 text-white font-bold px-5 py-2 transition-colors duration-200
              shadow-md focus:ring-2 focus:ring-pink-800 focus:ring-offset-2">
              Book Appointment
            </a>
          </nav>
          <!-- Star Section -->
          <aside data-aos="fade-up" data-aos-duration="800" class="py-6">
            <ul class="flex flex-wrap justify-center lg:justify-start gap-x-6 gap-y-4 text-center">
              <li v-for="(stat, index) in stats" :key="index" class="w-1/2 sm:w-auto">
                <strong class="text-2xl font-bold text-pink-600">{{ stat.value }}</strong>
                <small class="block text-sm text-gray-600"> {{stat.label }}</small>
              </li>
            </ul>
          </aside>
        </section>
        <!-- Hero Image -->
        <figure data-aos="fade-up" data-aos-delay="700" class="w-full lg:w-1/2
        flex justify-center relative">
          <div class="relative w-full max-w-xs sm:max-w-sm md:max-w-md">
            <span class="bg-pink-500 rounded-full w-64 g-64 sm:w-80 sm:h-80 absolute -top-10 -left-10
            opacity-20"></span>
             <span class="bg-purple-400 rounded-full w-48 g-48 sm:w-64 sm:h-64 absolute -bottom-10 -right-10
            opacity-20"></span>
            <img src="@assets/nurse.jpg"
                class="relative z-10 rounded-full shadow-2xl w-95 aspect-square object-cover"
                loading="eager"
            />
          </div>
        </figure>
      </article>
    </header>
</template>
