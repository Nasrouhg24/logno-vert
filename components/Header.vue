<template>
  <header class="w-full bg-white shadow-md fixed top-0 left-0 z-50">
    <nav class="max-w-7xl mx-auto flex items-center justify-between px-4 py-3">
      <NuxtLink to="/" class="flex items-center gap-2">
        <Icon name="mdi:sprout" class="text-green-700 text-3xl" />
        <span class="font-extrabold text-xl text-green-800 tracking-tight">LIGNO VERT</span>
      </NuxtLink>
      <div class="hidden md:flex gap-8 items-center">
        <NuxtLink to="/" class="nav-link">Accueil</NuxtLink>
        <NuxtLink to="/a-propos" class="nav-link">À propos</NuxtLink>
        <NuxtLink to="/services" class="nav-link">Services</NuxtLink>
        <NuxtLink to="/projets" class="nav-link">Projets</NuxtLink>
        <NuxtLink to="/contact" class="nav-link">Contact</NuxtLink>
      </div>
      <button @click="open = !open" class="md:hidden text-green-700 focus:outline-none">
        <Icon :name="open ? 'mdi:close' : 'mdi:menu'" class="text-3xl" />
      </button>
    </nav>
    <transition name="fade">
      <div v-if="open" class="md:hidden bg-white shadow-lg absolute w-full left-0 top-full flex flex-col items-center gap-4 py-4">
        <NuxtLink to="/" class="nav-link" @click="open = false">Accueil</NuxtLink>
        <NuxtLink to="/a-propos" class="nav-link" @click="open = false">À propos</NuxtLink>
        <NuxtLink to="/services" class="nav-link" @click="open = false">Services</NuxtLink>
        <NuxtLink to="/projets" class="nav-link" @click="open = false">Projets</NuxtLink>
        <NuxtLink to="/contact" class="nav-link" @click="open = false">Contact</NuxtLink>
      </div>
    </transition>
  </header>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const open = ref(false)
</script>

<style scoped>
.nav-link {
  @apply text-green-800 font-medium px-3 py-2 rounded hover:bg-green-50 transition;
}
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.3s;
}
.fade-enter-from, .fade-leave-to {
  opacity: 0;
}
</style> 