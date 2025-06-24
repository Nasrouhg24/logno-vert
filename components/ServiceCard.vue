<template>
  <div class="flex flex-col items-center p-6 bg-green-50 rounded-2xl shadow-lg hover:shadow-2xl transition group animate-fade-in-up">
    <Icon :name="service.icon" class="text-4xl text-green-700 mb-3 group-hover:scale-110 transition-transform" />
    <h3 class="font-bold text-lg mb-1 text-green-800">{{ service.title }}</h3>
    <p class="text-gray-700 text-center">{{ service.description }}</p>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue'
defineProps<{ service: { icon: string, title: string, description: string } }>()
</script> 