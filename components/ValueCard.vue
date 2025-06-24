<template>
  <div class="flex flex-col items-center p-6 bg-white rounded-2xl shadow-lg hover:shadow-2xl transition group animate-fade-in-up">
    <Icon :name="value.icon" class="text-4xl text-green-600 mb-3 group-hover:scale-110 transition-transform" />
    <h3 class="font-bold text-lg mb-1 text-green-800">{{ value.title }}</h3>
    <p class="text-gray-600 text-center">{{ value.desc }}</p>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue'
defineProps<{ value: { icon: string, title: string, desc: string } }>()
</script> 