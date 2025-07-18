<template>
  <section class="h-screen flex items-center justify-center text-center bg-gradient-to-br from-indigo-600 to-purple-700 text-white">
    <div ref="heroText" class="space-y-4">
      <h1 class="text-5xl font-bold">Hi, I'm Panharith</h1>
      <p class="text-xl">Web Developer & Sotfware Developer</p>
      <button class="px-6 py-2 bg-white text-indigo-700 rounded-full hover:scale-105 transition">See Projects</button>
    </div>
  </section>
</template>

<script setup>
import { onMounted, ref } from 'vue'
import { gsap } from 'gsap'

const heroText = ref(null)

onMounted(() => {
  gsap.from(heroText.value.children, {
    opacity: 0,
    y: 50,
    duration: 1,
    stagger: 0.3,
    ease: 'power2.out'
  })
})
</script>
