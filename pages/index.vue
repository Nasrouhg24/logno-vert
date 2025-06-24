<template>
  <div class="bg-gradient-to-br from-white via-lime-50 to-gray-100 min-h-screen font-sans">
    <!-- Hero Section -->
    <section class="relative flex flex-col items-center justify-center text-center min-h-[60vh] px-4 py-20">
      <h1 class="uppercase text-5xl md:text-7xl font-extrabold tracking-widest mb-6">
        <span class="text-[#8B5C2A]">LIGNO</span>
        <span class="text-green-700">VERT</span>
      </h1>
      <p class="text-xl md:text-2xl text-gray-700 mb-10 max-w-2xl mx-auto">Le futur du paysagisme et de l'entretien d'espaces verts au Maroc</p>
      <NuxtLink to="/contact" class="px-10 py-4 border-2 border-lime-400 text-lime-700 font-bold rounded-full bg-white/60 backdrop-blur-md shadow-lg hover:bg-lime-50 hover:scale-105 transition text-xl">Demander un devis</NuxtLink>
      <!-- Futuristic SVG wave -->
      <svg class="absolute bottom-0 left-0 w-full h-16 text-lime-100" viewBox="0 0 1440 320"><path fill="currentColor" fill-opacity="1" d="M0,224L1440,96L1440,320L0,320Z"></path></svg>
    </section>

    <!-- Services -->
    <section class="py-12 bg-white">
      <h2 class="text-3xl md:text-4xl font-bold text-lime-700 text-center mb-10 uppercase tracking-widest">Nos services</h2>
      <div class="flex flex-row gap-6 items-stretch justify-center overflow-x-auto max-w-full px-4 mx-auto">
        <div v-for="service in services" :key="service.title" class="flex flex-col items-center text-center bg-lime-50 rounded-xl shadow p-6 min-w-[220px] w-64">
          <span class="text-4xl mb-3">{{ service.icon }}</span>
          <h3 class="font-semibold text-lg text-lime-700 mb-2 uppercase tracking-wide">{{ service.title }}</h3>
          <p class="text-gray-600 text-sm">{{ service.description }}</p>
        </div>
      </div>
    </section>

    <!-- Points forts -->
    <section class="py-16 bg-gradient-to-r from-lime-50 via-white to-cyan-50">
      <h2 class="uppercase text-3xl md:text-4xl font-bold tracking-widest text-lime-700 text-center mb-12">Pourquoi nous choisir ?</h2>
      <div class="flex flex-row gap-6 items-stretch justify-center overflow-x-auto max-w-full px-4 mx-auto">
        <div v-for="point in pointsForts" :key="point.title" class="flex flex-col items-center text-center p-6 rounded-xl bg-white/80 border border-lime-100 shadow hover:shadow-xl hover:scale-105 hover:border-lime-400 transition min-w-[220px] w-64">
          <span class="inline-flex items-center justify-center w-10 h-10 rounded-full bg-gradient-to-br from-lime-200 to-lime-100 text-3xl mb-2">{{ point.icon }}</span>
          <h3 class="font-semibold text-lime-700 mb-1 uppercase tracking-wide">{{ point.title }}</h3>
          <p class="text-gray-600 text-sm">{{ point.desc }}</p>
        </div>
      </div>
    </section>

    <!-- Où nous trouver ? (carte) -->
    <section class="py-16 bg-gradient-to-br from-lime-50/80 via-white/80 to-cyan-50/80">
      <h2 class="uppercase text-2xl md:text-3xl font-bold tracking-widest text-lime-700 text-center mb-8">Où nous trouver&nbsp;?</h2>
      <div class="flex justify-center">
        <div class="w-full max-w-4xl rounded-2xl shadow-xl border border-green-200 overflow-hidden relative">
          <iframe
            src="https://www.google.com/maps?q=34.020882,-6.849813&hl=fr&z=16&output=embed"
            width="100%"
            height="500"
            style="border:0;"
            allowfullscreen=""
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"
            class="block w-full h-[300px] md:h-[500px]"
          ></iframe>
          <div class="absolute bottom-4 right-4 bg-white/90 rounded-xl shadow px-4 py-2 flex flex-col items-end gap-2 text-sm">
            <span class="text-green-700 font-bold">Ligno Vert</span>
            <span class="text-gray-700">Secteur 11, Rue Arrouz,<br>Centre d'Affaires Ryad Annakhil,<br>1er étage, N°24, Hay Ryad, Rabat.</span>
            <a
              href="https://www.google.com/maps/dir/?api=1&destination=Secteur+11%2C+Rue+Arrouz%2C+Centre+d'Affaires+Ryad+Annakhil%2C+1er+%C3%A9tage%2C+N%C2%B024%2C+Hay+Ryad%2C+Rabat"
              target="_blank"
              rel="noopener"
              class="mt-1 px-3 py-1 rounded bg-lime-100 text-green-800 font-semibold hover:bg-lime-200 transition"
            >
              Itinéraire
            </a>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA -->
    <div class="flex justify-center py-16">
      <NuxtLink to="/contact" class="px-12 py-4 border-2 border-lime-400 text-lime-700 font-bold rounded-full bg-white/70 backdrop-blur-md shadow-lg hover:bg-lime-50 hover:scale-105 transition text-2xl">Contact & Devis</NuxtLink>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const isVisible = ref(false)
function onIntersect(entries) {
  if (entries[0].isIntersecting) isVisible.value = true
}

const services = [
  { icon: '🪴', title: "Études et conceptions", description: "Développement de plans et designs innovants prenant en compte les contraintes techniques et environnementales." },
  { icon: '🏨', title: "Hôtels & Resorts", description: "Création de paysages accueillants pour une expérience haut de gamme (avec gestion responsable des ressources naturelles)." },
  { icon: '🏙️', title: "Voiries & aménagements urbains", description: "Embellissement de l'espace public via une approche durable et esthétique." },
  { icon: '🌳', title: "Entretien des espaces verts", description: "Suivi régulier des installations pour les maintenir dans un état optimal toute l'année." },
  { icon: '💧', title: "Réseaux d'arrosage", description: "Études et réalisation de systèmes d'irrigation adaptés, économes et efficaces." }
]

const pointsForts = [
  { icon: '🌱', title: "Expertise locale", desc: "Une équipe passionnée, enracinée dans le territoire marocain." },
  { icon: '🌿', title: "Solutions sur-mesure", desc: "Des projets adaptés à chaque client, chaque espace, chaque besoin." },
  { icon: '🤝', title: "Accompagnement complet", desc: "De la conception à l'entretien, un suivi personnalisé à chaque étape." },
  { icon: '🌍', title: "Engagement durable", desc: "Des pratiques respectueuses de l'environnement et des ressources naturelles." }
]
</script> 