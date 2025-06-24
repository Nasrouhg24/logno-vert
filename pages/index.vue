<template>
  <div class="bg-gradient-to-br from-lime-100 via-white to-amber-50 min-h-screen">
    <!-- Hero Section -->
    <section class="relative min-h-[70vh] flex items-center justify-center bg-cover bg-center" style="background-image: url('https://source.unsplash.com/1600x900/?nature,green,landscape');">
      <div class="absolute inset-0 bg-gradient-to-br from-lime-400/70 via-lime-300/60 to-amber-100/40 backdrop-blur-sm"></div>
      <div class="relative z-10 text-center flex flex-col items-center justify-center px-4 max-w-2xl mx-auto py-24">
        <h1 class="text-5xl md:text-7xl font-extrabold text-amber-700 tracking-tight drop-shadow-2xl mb-6 leading-tight">LIGNO <span class='text-lime-600'>VERT</span></h1>
        <p class="text-xl md:text-2xl text-amber-800/90 font-medium mb-10 leading-relaxed tracking-wide">Expert en paysagisme & entretien d'espaces verts au Maroc</p>
        <NuxtLink to="/contact" class="inline-block px-10 py-4 bg-gradient-to-r from-lime-400 via-lime-500 to-amber-300 hover:from-lime-500 hover:to-amber-200 text-amber-900 font-bold rounded-full shadow-xl ring-2 ring-offset-2 ring-lime-300 text-xl transition-all duration-300 ease-in-out focus:outline-none focus:ring-4 focus:ring-lime-400 hover:scale-105">Demander un devis</NuxtLink>
      </div>
    </section>

    <!-- Nos valeurs -->
    <section class="py-24 bg-gradient-to-b from-white/90 to-lime-50/80">
      <h2 class="text-4xl md:text-5xl font-extrabold text-center mb-14 text-lime-700 tracking-tight">Nos valeurs</h2>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-10 max-w-6xl mx-auto px-4">
        <div v-for="(value, i) in valeurs" :key="i" class="rounded-2xl border border-amber-100 bg-white/90 shadow-lg p-10 flex flex-col items-center text-center space-y-4 hover:shadow-2xl hover:-translate-y-2 transition-all duration-300 ease-in-out group">
          <span class="inline-flex items-center justify-center w-16 h-16 rounded-full bg-gradient-to-br from-lime-200 via-amber-100 to-lime-100 shadow text-4xl mb-2">{{ value.icon }}</span>
          <h3 class="font-bold text-lg text-amber-700 tracking-wide">{{ value.title }}</h3>
          <p class="text-amber-800 leading-relaxed text-balance">{{ value.desc }}</p>
        </div>
      </div>
    </section>

    <!-- Nos services -->
    <section class="py-24">
      <h2 class="text-4xl md:text-5xl font-extrabold text-center mb-14 text-lime-700 tracking-tight">Nos services</h2>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-10 max-w-6xl mx-auto px-4">
        <div v-for="(service, i) in services" :key="service.title" class="flex flex-col items-center text-center space-y-3 p-10 bg-white/90 rounded-2xl border border-amber-100 shadow-lg hover:shadow-2xl hover:-translate-y-2 transition-all duration-300 ease-in-out group">
          <span class="inline-flex items-center justify-center w-14 h-14 rounded-full bg-gradient-to-br from-lime-200 via-amber-100 to-lime-100 shadow text-3xl mb-2">{{ service.icon }}</span>
          <h3 class="font-bold text-lg text-amber-700 tracking-wide">{{ service.title }}</h3>
          <p class="text-amber-800 leading-relaxed text-balance">{{ service.description }}</p>
        </div>
      </div>
    </section>

    <!-- Couverture nationale -->
    <section class="py-24 bg-gradient-to-br from-lime-50/80 to-amber-50/80">
      <h2 class="text-4xl md:text-5xl font-extrabold text-center mb-14 text-lime-700 tracking-tight">Couverture nationale</h2>
      <div class="flex flex-col md:flex-row items-center justify-center gap-12 max-w-5xl mx-auto px-4">
        <div class="w-full md:w-1/2 rounded-2xl shadow-lg overflow-hidden ring-2 ring-amber-100 bg-white/90">
          <MapEmbed />
        </div>
        <ul class="text-lg space-y-6">
          <li v-for="zone in zones" :key="zone" class="flex items-center gap-4 text-lime-700 font-semibold tracking-wide">
            <span class="inline-block w-4 h-4 bg-lime-400 rounded-full ring-2 ring-amber-200"></span>
            {{ zone }}
          </li>
        </ul>
      </div>
    </section>

    <!-- CTA contact -->
    <div class="flex justify-center py-16">
      <NuxtLink to="/contact" class="px-14 py-6 bg-gradient-to-r from-lime-400 via-amber-200 to-amber-300 hover:from-lime-500 hover:to-amber-100 text-amber-900 font-extrabold rounded-full shadow-xl text-2xl tracking-wide ring-2 ring-offset-2 ring-lime-300 transition-all duration-300 ease-in-out focus:outline-none focus:ring-4 focus:ring-lime-400 hover:scale-105">Contactez-nous</NuxtLink>
    </div>
  </div>
</template>

<script setup lang="ts">
import MapEmbed from '~/components/MapEmbed.vue'

const valeurs = [
  { icon: '🌱', title: "L'humain en premier", desc: "Valorisation des collaborateurs, bien-être et sécurité au travail." },
  { icon: '🤝', title: "Travail en équipe", desc: "Synergie et collaboration sur chaque projet." },
  { icon: '🔗', title: "Partage de l'information", desc: "Culture d'amélioration continue par la transmission du savoir." },
  { icon: '🌍', title: "Communautés élargies", desc: "Acteur de développement local (revendeurs, fournisseurs)." },
  { icon: '💚', title: "Relations fortes", desc: "Relations durables et professionnelles avec les partenaires." }
]

const services = [
  { icon: '🪴', title: "Études et conceptions", description: "Développement de plans et designs innovants prenant en compte les contraintes techniques et environnementales." },
  { icon: '🏨', title: "Hôtels & Resorts", description: "Création de paysages accueillants pour une expérience haut de gamme (avec gestion responsable des ressources naturelles)." },
  { icon: '🏙️', title: "Voiries & aménagements urbains", description: "Embellissement de l'espace public via une approche durable et esthétique." },
  { icon: '🌳', title: "Entretien des espaces verts", description: "Suivi régulier des installations pour les maintenir dans un état optimal toute l'année." },
  { icon: '💧', title: "Réseaux d'arrosage", description: "Études et réalisation de systèmes d'irrigation adaptés, économes et efficaces." }
]

const zones = [
  "Zone Nord-Est",
  "Zone Centre",
  "Zone Sud",
  "Siège à Rabat"
]
</script> 