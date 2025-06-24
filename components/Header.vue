<template>
  <header class="w-full bg-white shadow-md fixed top-0 left-0 z-50">
    <nav class="max-w-7xl mx-auto flex items-center justify-between px-4 py-3">
      <NuxtLink to="/" class="flex items-center gap-2">
        <span class="text-green-700 text-3xl">🌱</span>
        <span class="font-extrabold text-xl text-green-800 tracking-tight">LIGNO VERT</span>
      </NuxtLink>
      <div class="hidden md:flex gap-8 items-center">
        <NuxtLink to="/" class="text-green-800 font-medium px-3 py-2 rounded hover:bg-green-50 transition">Accueil</NuxtLink>
        <NuxtLink to="/a-propos" class="text-green-800 font-medium px-3 py-2 rounded hover:bg-green-50 transition">À propos</NuxtLink>
        <NuxtLink to="/services" class="text-green-800 font-medium px-3 py-2 rounded hover:bg-green-50 transition">Services</NuxtLink>
        <NuxtLink to="/projets" class="text-green-800 font-medium px-3 py-2 rounded hover:bg-green-50 transition">Projets</NuxtLink>
        <NuxtLink to="/contact" class="text-green-800 font-medium px-3 py-2 rounded hover:bg-green-50 transition">Contact</NuxtLink>
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
const open = ref(false)
</script> 