<template>
  <div class="flex flex-col items-center p-6 bg-white/10 backdrop-blur rounded-3xl shadow-2xl ring-1 ring-emerald-300/30 border border-lime-200/20 hover:scale-105 hover:shadow-green-400/50 hover:-translate-y-1 hover:rotate-1 transition-transform duration-300 space-y-4">
    <span class="w-14 h-14 flex items-center justify-center bg-emerald-200 rounded-full text-3xl mb-2 animate-pulse">{{ service.icon }}</span>
    <h3 class="font-bold text-lg text-green-800 tracking-wide">{{ service.title }}</h3>
    <p class="text-gray-700 text-balance tracking-wide">{{ service.description }}</p>
    <button class="mt-2 text-sm uppercase font-bold tracking-wide bg-emerald-100 text-green-800 rounded-full px-4 py-2 shadow hover:bg-green-800 hover:text-white transition">Découvrir</button>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue'
defineProps<{ service: { icon: string, title: string, description: string } }>()
</script> 