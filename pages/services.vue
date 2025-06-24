<template>
  <div class="max-w-6xl mx-auto py-16 px-4">
    <h1 class="text-4xl font-bold mb-12 text-green-700 tracking-wide">Nos services</h1>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-12">
      <div v-for="(service, i) in services" :key="service.title" class="flex flex-col items-center text-center space-y-4 p-8 bg-white/80 rounded-2xl border-l-4 border-green-500 shadow-xl hover:shadow-2xl hover:scale-105 transition-all duration-300 ease-in-out opacity-0 translate-y-10 animate-fade-in" :style="`animation-delay: ${i * 120}ms`">
        <span class="inline-flex items-center justify-center w-14 h-14 rounded-full bg-green-700/90 shadow mb-2 text-3xl">
          {{ service.icon }}
        </span>
        <h3 class="font-bold text-lg text-green-900 tracking-wide">{{ service.title }}</h3>
        <p class="text-gray-700 leading-relaxed text-balance">{{ service.description }}</p>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const services = [
  { icon: '✏️', title: "Études et conceptions", description: "Développement de plans et designs innovants prenant en compte les contraintes techniques et environnementales." },
  { icon: '🏨', title: "Hôtels & Resorts", description: "Création de paysages accueillants pour une expérience haut de gamme (avec gestion responsable des ressources naturelles)." },
  { icon: '🏙️', title: "Voiries & aménagements urbains", description: "Embellissement de l'espace public via une approche durable et esthétique." },
  { icon: '🌱', title: "Entretien des espaces verts", description: "Suivi régulier des installations pour les maintenir dans un état optimal toute l'année." },
  { icon: '💧', title: "Réseaux d'arrosage", description: "Études et réalisation de systèmes d'irrigation adaptés, économes et efficaces." }
]
</script>

<style>
@layer utilities {
  .animate-fade-in {
    animation: fadeInUp 1s cubic-bezier(0.22, 1, 0.36, 1) both;
  }
  @keyframes fadeInUp {
    0% {
      opacity: 0;
      transform: translateY(40px);
    }
    100% {
      opacity: 1;
      transform: translateY(0);
    }
  }
}
</style>

 