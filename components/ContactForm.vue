<template>
  <form class="space-y-4 animate-fade-in-up" @submit.prevent="submitForm">
    <div>
      <label class="block text-sm font-medium text-green-800 mb-1">Nom</label>
      <input v-model="form.nom" type="text" required class="w-full px-4 py-2 rounded-lg border border-green-200 focus:ring-2 focus:ring-green-400 outline-none" />
    </div>
    <div>
      <label class="block text-sm font-medium text-green-800 mb-1">Email</label>
      <input v-model="form.email" type="email" required class="w-full px-4 py-2 rounded-lg border border-green-200 focus:ring-2 focus:ring-green-400 outline-none" />
    </div>
    <div>
      <label class="block text-sm font-medium text-green-800 mb-1">Message</label>
      <textarea v-model="form.message" required rows="4" class="w-full px-4 py-2 rounded-lg border border-green-200 focus:ring-2 focus:ring-green-400 outline-none"></textarea>
    </div>
    <button type="submit" class="w-full py-3 bg-green-700 text-white rounded-lg font-semibold shadow hover:bg-green-800 transition">Envoyer</button>
    <p v-if="sent" class="text-green-700 mt-2">Merci pour votre message !</p>
  </form>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const form = ref({ nom: '', email: '', message: '' })
const sent = ref(false)
function submitForm() {
  sent.value = true
  setTimeout(() => { sent.value = false }, 4000)
  form.value = { nom: '', email: '', message: '' }
}
</script> 