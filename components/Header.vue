<template>
  <header class="w-full fixed top-0 left-0 z-50 bg-gradient-to-r from-lime-50 via-white to-amber-50 shadow-2xl rounded-b-2xl">
    <nav class="max-w-7xl mx-auto flex items-center justify-between px-6 py-5">
      <NuxtLink to="/" class="flex items-center gap-3 group transition-transform duration-200 hover:scale-105">
        <img src="/logo-lignovert.png" alt="Logo Ligno Vert" class="w-10 h-10 md:w-12 md:h-12 object-contain" />
      </NuxtLink>
      <div class="flex gap-3 md:gap-10 items-center overflow-x-auto max-w-full scrollbar-thin scrollbar-thumb-lime-200">
        <NuxtLink to="/" class="nav-link text-base md:text-lg px-2 md:px-4" :class="{ 'active-link': $route.path === '/' }">Accueil</NuxtLink>
        <NuxtLink to="/a-propos" class="nav-link text-base md:text-lg px-2 md:px-4" :class="{ 'active-link': $route.path === '/a-propos' }">À propos</NuxtLink>
        <NuxtLink to="/services" class="nav-link text-base md:text-lg px-2 md:px-4" :class="{ 'active-link': $route.path === '/services' }">Services</NuxtLink>
        <NuxtLink to="/projets" class="nav-link text-base md:text-lg px-2 md:px-4" :class="{ 'active-link': $route.path === '/projets' }">Projets</NuxtLink>
        <NuxtLink to="/contact" class="nav-link text-base md:text-lg px-2 md:px-4" :class="{ 'active-link': $route.path === '/contact' }">Contact</NuxtLink>
      </div>
    </nav>
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
  @apply text-green-900 font-semibold px-4 py-2 rounded-lg hover:text-yellow-600 hover:bg-green-100 transition text-lg;
}
.active-link {
  @apply bg-yellow-100 text-yellow-700 shadow font-bold;
}
.nav-link-mobile {
  @apply text-green-800 font-semibold text-xl px-6 py-3 rounded-lg hover:bg-lime-100 hover:text-lime-700 transition w-full text-center;
}
</style> 