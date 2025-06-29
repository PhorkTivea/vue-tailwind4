<template>
  <header class="relative bg-gradient-to-r from-pink-100 to-purple-100 top-0 z-50">
    <div class="max-w-screen-xl mx-auto px-4 py-4 flex justify-between items-center">
      <a href="/" class="flex items-center focus:outline-none focus:ring-2 focus:ring-pink-600 rounded">
        <h1 class="text-xl font-bold text-pink-600">Hello Clinic</h1>
      </a>
      <nav class="hidden md:flex space-x-4">
        <a
            v-for="(item, index) in navLinks"
            :key="index"
            :href="item.href"
            class="text-gray-700 hover:text-pink-600 transition-colors duration-200 focus:outline-none focus:ring-2 focus:ring-pink-600 rounded"
        >
          {{ item.label }}
        </a>
      </nav>
      <div class="hidden md:block">
        <a href="#appointment" class="bg-pink-600 hover:bg-pink-700 text-white font-bold px-5 py-2 transition-colors duration-200
        shadow-md focus:ring-2 focus:ring-pink-800 focus:ring-offset-2">
          Book Appointment
        </a>
      </div>
      <!--  Mobile Menu btn    -->
      <button class="md:hidden p-2 focus:outline-none focus:ring-2 focus:ring-pink-600 rounded"
      @click="onToggle" aria-label="Toggle Menu" :aria-expanded="isMenuOpen" aria-controls="mobile-menu">
        <Icon :icon="isMenuOpen ? 'mdi:close' : 'mdi:menu'" class="w-6 h-6"></Icon>
      </button>
    </div>
    <aside v-if="isMenuOpen"
    id="mobile-menu"
    class="md:hidden bg-white shadow-lg py-4 px-4 absolute top-full left-0 right-0 z-40"
     aria-label="Mobile Menu"
    >
      <nav aria-label="Mobile Navigation">
        <ul>
          <li v-for="(item, index) in navLinks" :key="index">
            <a :href="item.href"
            class="block text-gray-700 hover:text-pink-600 transition-colors duration-200 px-2 py-2 focus:outline-none focus:ring-2 focus:ring-pink-600 rounded"
            >
              {{ item.label}}
            </a>
          </li>
        </ul>
      </nav>
    </aside>
  </header>
</template>

<script setup lang="ts">
const navLinks = ref([
  {href: '#home', label: 'Home'},
  {href: '#services', label: 'Services'},
  {href: '#about', label: 'About'},
  {href: '#specailist', label: 'Specialists'},
  {href: '#contact', label: 'Contact'},
])
const isMenuOpen = ref(false)

function onToggle() {
  isMenuOpen.value = !isMenuOpen.value
}
</script>
