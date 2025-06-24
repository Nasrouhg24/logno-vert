<template>
  <NuxtLink :to="`/projets/${projet.slug}`" class="block bg-white/90 rounded-2xl border border-green-100 shadow-lg hover:shadow-2xl hover:scale-105 transition-all duration-300 group overflow-hidden animate-fade-in">
    <img :src="projet.image" :alt="projet.title" class="w-full h-40 object-cover group-hover:scale-105 transition-transform duration-300" />
    <div class="p-4">
      <h3 class="font-bold text-lg text-green-800 mb-1">{{ projet.title }}</h3>
      <p class="text-sm text-gray-600 mb-2">{{ projet.client }}</p>
      <div class="flex justify-between text-xs text-gray-500 items-center gap-2">
        <span class="flex items-center gap-1">
          <svg class="w-4 h-4 text-green-700" fill="currentColor" viewBox="0 0 24 24"><path d="M12,6A6,6 0 0,1 18,12C18,16.5 12,22 12,22C12,22 6,16.5 6,12A6,6 0 0,1 12,6M12,8A4,4 0 0,0 8,12A4,4 0 0,0 12,16A4,4 0 0,0 16,12A4,4 0 0,0 12,8Z"/></svg>
          {{ projet.location }}
        </span>
        <span class="flex items-center gap-1">
          <svg class="w-4 h-4 text-green-700" fill="currentColor" viewBox="0 0 24 24"><path d="M19,4H18V2H16V4H8V2H6V4H5A2,2 0 0,0 3,6V20A2,2 0 0,0 5,22H19A2,2 0 0,0 21,20V6A2,2 0 0,0 19,4M19,20H5V9H19V20M7,11H9V13H7V11M11,11H13V13H11V11M15,11H17V13H15V11Z"/></svg>
          {{ projet.date }}
        </span>
      </div>
    </div>
  </NuxtLink>
</template>

<script setup lang="ts">
import { defineProps } from 'vue'
defineProps<{ projet: { slug: string, title: string, client: string, location: string, date: string, image: string } }>()
</script> 