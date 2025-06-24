<template>
  <div class="max-w-6xl mx-auto py-16 px-4">
    <h1 class="text-4xl font-bold mb-8 text-green-700">Nos réalisations</h1>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
      <ProjectCard v-for="projet in projets" :key="projet.title" :projet="projet" />
    </div>
  </div>
</template>

<script setup lang="ts">
import ProjectCard from '~/components/ProjectCard.vue'
const projets = [
  { slug: 'banque-mondiale-fmi', title: 'Assemblées Générales Banque Mondiale & FMI', client: 'Ministère des Affaires Étrangères', location: 'Bab Ighli, Marrakech', date: '2023', description: 'Aménagement paysager du village des assemblées à Bab Ighli, Marrakech.', image: 'https://source.unsplash.com/400x300/?landscape,morocco' },
  { slug: 'station-saidia', title: 'Nouvelle station touristique de Saidia – Corniche', client: 'SDS (Société de Développement de Saidia)', location: 'Saidia', date: '2021', description: 'Entretien de la corniche.', image: 'https://source.unsplash.com/400x300/?beach,morocco' },
  { slug: 'melia-beach', title: 'Hôtel Melia Beach 5*', client: 'SDS – Saidia', location: 'Saidia', date: '2020', description: 'Aménagement paysager des espaces extérieurs.', image: 'https://source.unsplash.com/400x300/?hotel,garden' },
  { slug: 'hyatt-regency', title: 'Hyatt Regency 5*', client: 'MADAEF – Taghazout Bay', location: 'Taghazout Bay', date: '2021', description: 'Aménagement paysager extérieur.', image: 'https://source.unsplash.com/400x300/?hyatt,landscape' },
  { slug: 'hilton-taghazout', title: 'Hôtel Hilton Taghazout Bay 5*', client: 'SAPST – Taghazout', location: 'Taghazout', date: '2022', description: 'Aménagement paysager extérieur.', image: 'https://source.unsplash.com/400x300/?hilton,landscape' }
]
</script> 