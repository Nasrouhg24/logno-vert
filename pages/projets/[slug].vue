<template>
  <div class="max-w-4xl mx-auto py-16 px-4">
    <h1 class="text-4xl font-bold mb-6 text-green-700">{{ projet.title }}</h1>
    <div class="mb-8 flex flex-col md:flex-row gap-8">
      <div class="flex-1">
        <div v-if="projet.images && projet.images.length" class="mb-4">
          <div class="flex gap-2 overflow-x-auto">
            <img v-for="(img, i) in projet.images" :key="i" :src="img" :alt="projet.title" class="rounded-xl shadow w-64 h-40 object-cover transition-transform hover:scale-105 duration-300" />
          </div>
        </div>
        <p class="text-lg mb-2">{{ projet.description }}</p>
        <ul class="text-sm text-gray-700 space-y-1">
          <li><strong>Client :</strong> {{ projet.client }}</li>
          <li><strong>Lieu :</strong> {{ projet.location }}</li>
          <li><strong>Date :</strong> {{ projet.date }}</li>
        </ul>
      </div>
    </div>
    <section class="mt-12">
      <h2 class="text-2xl font-semibold mb-4">Projets similaires</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
        <ProjectCard v-for="p in projetsSimilaires" :key="p.slug" :projet="p" />
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
import { useRoute } from 'vue-router'
import ProjectCard from '~/components/ProjectCard.vue'

const route = useRoute()
// Placeholder: à remplacer par une vraie récupération du contenu
const projets = [
  { slug: 'banque-mondiale-fmi', title: 'Assemblées Générales Banque Mondiale & FMI', client: 'Ministère des Affaires Étrangères', location: 'Bab Ighli, Marrakech', date: '2023', description: 'Aménagement paysager du village des assemblées à Bab Ighli, Marrakech.', images: ['https://source.unsplash.com/800x600/?landscape,morocco','https://source.unsplash.com/800x600/?garden'], type: 'urbain' },
  { slug: 'station-saidia', title: 'Nouvelle station touristique de Saidia – Corniche', client: 'SDS (Société de Développement de Saidia)', location: 'Saidia', date: '2021', description: 'Entretien de la corniche.', images: ['https://source.unsplash.com/800x600/?beach,morocco','https://source.unsplash.com/800x600/?corniche'], type: 'hôtellerie' },
  { slug: 'melia-beach', title: 'Hôtel Melia Beach 5*', client: 'SDS – Saidia', location: 'Saidia', date: '2020', description: 'Aménagement paysager des espaces extérieurs.', images: ['https://source.unsplash.com/800x600/?hotel,garden','https://source.unsplash.com/800x600/?resort'], type: 'hôtellerie' },
  { slug: 'hyatt-regency', title: 'Hyatt Regency 5*', client: 'MADAEF – Taghazout Bay', location: 'Taghazout Bay', date: '2021', description: 'Aménagement paysager extérieur.', images: ['https://source.unsplash.com/800x600/?hyatt,landscape','https://source.unsplash.com/800x600/?hotel'], type: 'hôtellerie' },
  { slug: 'hilton-taghazout', title: 'Hôtel Hilton Taghazout Bay 5*', client: 'SAPST – Taghazout', location: 'Taghazout', date: '2022', description: 'Aménagement paysager extérieur.', images: ['https://source.unsplash.com/800x600/?hilton,landscape','https://source.unsplash.com/800x600/?hotel'], type: 'hôtellerie' }
]
const projet = projets.find(p => p.slug === route.params.slug) || projets[0]
const projetsSimilaires = projets.filter(p => p.type === projet.type && p.slug !== projet.slug).slice(0,2)
</script> 