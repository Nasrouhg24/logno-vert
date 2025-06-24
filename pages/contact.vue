<template>
  <div class="max-w-3xl mx-auto py-16 px-4">
    <h1 class="text-4xl font-bold mb-8 text-green-700">Contactez-nous</h1>
    <div class="grid md:grid-cols-2 gap-8">
      <div>
        <ContactForm />
        <div class="mt-8 text-sm text-gray-700">
          <p><strong>Téléphone :</strong> 05 37 77 12 49</p>
          <p><strong>Email :</strong> <a href="mailto:contact@lignovert.ma" class="text-green-700 underline">contact@lignovert.ma</a></p>
          <p><strong>Adresse :</strong><br>Secteur 11, Rue Arrouz,<br>Centre d'Affaires Ryad Annakhil,<br>1er étage, N°24, Hay Ryad, Rabat.</p>
        </div>
      </div>
      <div>
        <MapEmbed class="rounded-xl shadow h-64 w-full" />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import ContactForm from '~/components/ContactForm.vue'
import MapEmbed from '~/components/MapEmbed.vue'
</script> 