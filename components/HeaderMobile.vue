<template>
  <header class="w-full bg-green-900 text-green-100 py-5 px-4 flex items-center justify-between shadow-md min-h-[70px]">
    <img src="/logo-lignovert.png" alt="Logo Ligno Vert" class="w-10 h-10 object-contain mx-auto" />
    <button @click="open = !open" class="text-2xl text-green-100 focus:outline-none">
      <span v-if="!open">☰</span>
      <span v-else>✖️</span>
    </button>
    <transition name="fade">
      <nav v-if="open" class="absolute top-[70px] left-0 w-full bg-green-950 text-green-100 flex flex-col items-center gap-3 py-6 z-50 shadow-lg">
        <NuxtLink to="/" class="text-sm font-semibold" @click="open = false">Accueil</NuxtLink>
        <NuxtLink to="/a-propos" class="text-sm font-semibold" @click="open = false">À propos</NuxtLink>
        <NuxtLink to="/services" class="text-sm font-semibold" @click="open = false">Services</NuxtLink>
        <NuxtLink to="/projets" class="text-sm font-semibold" @click="open = false">Projets</NuxtLink>
        <NuxtLink to="/contact" class="text-sm font-semibold" @click="open = false">Contact</NuxtLink>
      </nav>
    </transition>
  </header>
</template>

<script setup>
import { ref } from 'vue'
const open = ref(false)
</script> 