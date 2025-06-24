<template>
  <div class="flex flex-col items-center p-6 bg-white/10 backdrop-blur rounded-3xl shadow-2xl ring-1 ring-emerald-300/30 border border-lime-200/20 hover:scale-105 hover:shadow-green-400/50 hover:-translate-y-1 hover:rotate-1 transition-transform duration-300 space-y-4">
    <span class="w-14 h-14 flex items-center justify-center bg-emerald-200 rounded-full text-3xl mb-2 animate-pulse">{{ value.icon }}</span>
    <h3 class="font-bold text-lg text-green-800 tracking-wide">{{ value.title }}</h3>
    <p class="text-gray-600 text-balance tracking-wide">{{ value.desc }}</p>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue'
defineProps<{ value: { icon: string, title: string, desc: string } }>()
</script> 