<template>
    <section ref="heroText"
        class="h-screen flex items-center justify-center text-center bg-gradient-to-br from-indigo-600 to-purple-700 text-white">
        <div class="space-y-4">
            <h1 class="text-5xl font-bold">Hi, I'm Panharith</h1>
            <p class="text-xl">Web Developer & Sotfware Developer</p>
            <!-- <button class="px-6 py-2 bg-white text-indigo-700 rounded-full hover:scale-105 transition">See Projects</button> -->

            <a href="/Sor Panharith.pdf" download class=" items-center m-4">
                <ButtonItem btnName="GET CV" />
            </a>

        </div>
        <div class="ml-2.5 rounded-2xl border-2 ">
            <p align="center">
                <img class="rounded-2xl" src="https://media.tenor.com/2uyENRmiUt0AAAAC/coding.gif" alt="Anime Typing"
                    width="500" />
            </p>
        </div>
    </section>
</template>

<script setup>
import { onMounted, ref } from 'vue'
import { gsap } from 'gsap'
import ButtonItem from '../material/ButtonItem.vue'
const heroText = ref(null)

onMounted(() => {
    gsap.from(heroText.value.children, {
        opacity: 0,
        y: 50,
        duration: 2,
        stagger: 0.3,
        ease: 'power2.out'
    })
})

const images = [
  'https://media.tenor.com/2uyENRmiUt0AAAAC/coding.gif',
  'https://media.tenor.com/LoUEbsBKwT0AAAAd/code.gif',
  'https://media.tenor.com/kX2bOUxKXHIAAAAd/programming.gif',
  'https://media.tenor.com/IHdlTRsmcS4AAAAC/programming.gif',
]
const activeIndex = ref(0)
const next = () => {
  activeIndex.value = (activeIndex.value + 1) % images.length
}
const next = () => {
  activeIndex.value = (activeIndex.value + 1) % images.length
}

const prev = () => {
  activeIndex.value = (activeIndex.value - 1 + images.length) % images.length
}
</script>
