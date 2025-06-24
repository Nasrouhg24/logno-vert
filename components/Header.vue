<template>
  <header class="w-full fixed top-0 left-0 z-50 bg-gradient-to-r from-lime-50 via-white to-amber-50 shadow-2xl rounded-b-2xl">
    <nav class="max-w-7xl mx-auto flex items-center justify-between px-6 py-5">
      <NuxtLink to="/" class="flex items-center gap-3 group transition-transform duration-200 hover:scale-105">
        <span class="text-green-700 text-4xl">🌱</span>
        <span class="font-extrabold text-2xl text-green-800 tracking-tight group-hover:text-lime-600 transition">LIGNO VERT</span>
      </NuxtLink>
      <div class="flex gap-10 items-center">
        <NuxtLink to="/" class="nav-link" :class="{ 'active-link': $route.path === '/' }">Accueil</NuxtLink>
        <NuxtLink to="/a-propos" class="nav-link" :class="{ 'active-link': $route.path === '/a-propos' }">À propos</NuxtLink>
        <NuxtLink to="/services" class="nav-link" :class="{ 'active-link': $route.path === '/services' }">Services</NuxtLink>
        <NuxtLink to="/projets" class="nav-link" :class="{ 'active-link': $route.path === '/projets' }">Projets</NuxtLink>
        <NuxtLink to="/contact" class="nav-link" :class="{ 'active-link': $route.path === '/contact' }">Contact</NuxtLink>
      </div>
      <button @click="open = !open" class="md:hidden text-green-700 focus:outline-none text-3xl">
        <span v-if="!open">☰</span>
        <span v-else>✖️</span>
      </button>
    </nav>
    <transition name="fade">
      <div v-if="open" class="md:hidden bg-white shadow-lg absolute w-full left-0 top-full flex flex-col items-center gap-4 py-4">
        <NuxtLink to="/" class="text-green-800 font-medium px-3 py-2 rounded hover:bg-green-50 transition" @click="open = false">Accueil</NuxtLink>
        <NuxtLink to="/a-propos" class="text-green-800 font-medium px-3 py-2 rounded hover:bg-green-50 transition" @click="open = false">À propos</NuxtLink>
        <NuxtLink to="/services" class="text-green-800 font-medium px-3 py-2 rounded hover:bg-green-50 transition" @click="open = false">Services</NuxtLink>
        <NuxtLink to="/projets" class="text-green-800 font-medium px-3 py-2 rounded hover:bg-green-50 transition" @click="open = false">Projets</NuxtLink>
        <NuxtLink to="/contact" class="text-green-800 font-medium px-3 py-2 rounded hover:bg-green-50 transition" @click="open = false">Contact</NuxtLink>
      </div>
    </transition>
  </header>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import { useRoute } from 'vue-router'
const open = ref(false)
const $route = useRoute()
</script>

<style lang="postcss" scoped>
.nav-link {
  @apply text-green-800 font-semibold px-4 py-2 rounded-lg hover:bg-lime-100 hover:text-lime-700 transition text-lg;
}
.active-link {
  @apply bg-lime-200 text-lime-800 shadow font-bold;
}
</style> 