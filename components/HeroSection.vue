<template>
  <section class="relative flex flex-col items-center justify-center text-center py-20 bg-gradient-to-br from-green-100 to-green-300 overflow-hidden">
    <div class="z-10 animate-fade-in-up">
      <h1 class="text-5xl md:text-6xl font-extrabold text-green-800 mb-4 drop-shadow-lg">LIGNO VERT</h1>
      <p class="text-xl md:text-2xl text-green-900 mb-8 font-medium">Expert en paysagisme & entretien d'espaces verts au Maroc</p>
      <NuxtLink to="/contact" class="inline-block px-8 py-4 bg-green-700 text-white rounded-full shadow-lg text-lg font-semibold hover:bg-green-800 transition">Demander un devis</NuxtLink>
    </div>
    <img src="https://source.unsplash.com/1200x500/?nature,greenery" alt="Nature" class="absolute inset-0 w-full h-full object-cover opacity-30 pointer-events-none" />
    <div class="absolute bottom-0 left-0 w-full h-32 bg-gradient-to-t from-green-100 to-transparent"></div>
  </section>
</template>

<script setup lang="ts">
// Animation fade-in-up avec Tailwind (à ajouter dans tailwind.config.js si besoin)
</script> 