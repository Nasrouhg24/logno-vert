<template>
  <NuxtLink :to="`/projets/${projet.slug}`" class="block bg-white/10 backdrop-blur rounded-3xl border border-lime-200/20 shadow-2xl ring-1 ring-emerald-300/30 hover:scale-105 hover:shadow-green-400/50 hover:-translate-y-1 transition-transform duration-300 group overflow-hidden">
    <img :src="projet.image" :alt="projet.title" class="w-full h-56 object-cover rounded-t-3xl group-hover:scale-105 transition-transform duration-300" />
    <div class="p-6 space-y-4">
      <h3 class="font-bold text-lg text-green-800 mb-1 tracking-wide">{{ projet.title }}</h3>
      <p class="text-sm text-gray-600 mb-2 text-balance">{{ projet.client }}</p>
      <div class="flex justify-between text-xs text-gray-500 items-center gap-2">
        <span class="flex items-center gap-1 bg-emerald-200 rounded-full px-3 py-1">{{ projet.location }}</span>
        <span class="flex items-center gap-1 bg-emerald-200 rounded-full px-3 py-1">{{ projet.date }}</span>
      </div>
    </div>
  </NuxtLink>
</template>

<script setup lang="ts">
import { defineProps } from 'vue'
defineProps<{ projet: { slug: string, title: string, client: string, location: string, date: string, image: string } }>()
</script> 