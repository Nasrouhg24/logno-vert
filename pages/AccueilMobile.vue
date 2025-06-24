<template>
  <div class="bg-gradient-to-b from-white via-lime-50 to-gray-100 min-h-screen font-sans">
    <!-- Hero Section -->
    <section class="flex flex-col items-center justify-center text-center min-h-[40vh] px-2 py-8">
      <img src="/logo-lignovert.png" alt="Logo Ligno Vert" class="w-20 h-20 mb-2 mx-auto" />
      <h1 class="uppercase text-3xl font-extrabold tracking-widest mb-3">
        <span class="text-[#8B5C2A]">LIGNO</span>
        <span class="text-green-700">VERT</span>
      </h1>
      <p class="text-base text-gray-700 mb-6 max-w-xs mx-auto">Le futur du paysagisme et de l'entretien d'espaces verts au Maroc</p>
      <NuxtLink to="/contact" class="px-6 py-3 border-2 border-lime-400 text-lime-700 font-bold rounded-full bg-white/60 backdrop-blur-md shadow-lg hover:bg-lime-50 hover:scale-105 transition text-base">Demander un devis</NuxtLink>
    </section>
    <!-- Services -->
    <section class="py-6 bg-white">
      <h2 class="text-2xl font-bold text-lime-700 text-center mb-6 uppercase tracking-widest">Nos services</h2>
      <div class="flex flex-col gap-4 items-stretch px-2">
        <div v-for="service in services" :key="service.title" class="flex flex-row items-center bg-lime-50 rounded-xl shadow p-4">
          <span class="text-2xl mr-3">{{ service.icon }}</span>
          <div>
            <h3 class="font-semibold text-base text-lime-700 mb-1 uppercase tracking-wide">{{ service.title }}</h3>
            <p class="text-gray-600 text-xs">{{ service.description }}</p>
          </div>
        </div>
      </div>
    </section>
    <!-- Points forts -->
    <section class="py-8 bg-gradient-to-b from-lime-50 via-white to-cyan-50">
      <h2 class="uppercase text-2xl font-bold tracking-widest text-lime-700 text-center mb-6">Pourquoi nous choisir ?</h2>
      <div class="flex flex-col gap-4 items-stretch px-2">
        <div v-for="point in pointsForts" :key="point.title" class="flex flex-row items-center p-4 rounded-xl bg-white/80 border border-lime-100 shadow">
          <span class="inline-flex items-center justify-center w-8 h-8 rounded-full bg-gradient-to-br from-lime-200 to-lime-100 text-xl mr-3">{{ point.icon }}</span>
          <div>
            <h3 class="font-semibold text-lime-700 mb-1 uppercase tracking-wide text-sm">{{ point.title }}</h3>
            <p class="text-gray-600 text-xs">{{ point.desc }}</p>
          </div>
        </div>
      </div>
    </section>
    <!-- Où nous trouver ? (carte) -->
    <section class="py-8 bg-gradient-to-b from-lime-50/80 via-white/80 to-cyan-50/80">
      <h2 class="uppercase text-xl font-bold tracking-widest text-lime-700 text-center mb-4">Où nous trouver&nbsp;?</h2>
      <div class="flex justify-center">
        <div class="w-full max-w-xs rounded-xl shadow-xl border border-green-200 overflow-hidden relative">
          <iframe
            src="https://www.google.com/maps?q=34.020882,-6.849813&hl=fr&z=16&output=embed"
            width="100%"
            height="180"
            style="border:0;"
            allowfullscreen=""
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"
            class="block w-full h-[120px]"
          ></iframe>
          <div class="absolute bottom-2 right-2 bg-white/90 rounded-xl shadow px-2 py-1 flex flex-col items-end gap-1 text-xs">
            <span class="text-green-700 font-bold">Ligno Vert</span>
            <span class="text-gray-700">Secteur 11, Rue Arrouz,<br>Centre d'Affaires Ryad Annakhil,<br>1er étage, N°24, Hay Ryad, Rabat.</span>
            <a
              href="https://www.google.com/maps/dir/?api=1&destination=Secteur+11%2C+Rue+Arrouz%2C+Centre+d'Affaires+Ryad+Annakhil%2C+1er+%C3%A9tage%2C+N%C2%B024%2C+Hay+Ryad%2C+Rabat"
              target="_blank"
              rel="noopener"
              class="mt-1 px-2 py-1 rounded bg-lime-100 text-green-800 font-semibold hover:bg-lime-200 transition text-xs"
            >
              Itinéraire
            </a>
          </div>
        </div>
      </div>
    </section>
    <!-- CTA -->
    <div class="flex justify-center py-8">
      <NuxtLink to="/contact" class="px-6 py-3 border-2 border-lime-400 text-lime-700 font-bold rounded-full bg-white/70 backdrop-blur-md shadow-lg hover:bg-lime-50 hover:scale-105 transition text-base">Contact & Devis</NuxtLink>
    </div>
  </div>
</template>

<script setup>
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