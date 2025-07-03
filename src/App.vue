<script setup lang="ts">
import AOS from 'aos'
import 'aos/dist/aos.css'

onMounted(() => {
  AOS.init()
})
</script>

<template>
  <Header />
  <Hero />
  <Service />
</template>