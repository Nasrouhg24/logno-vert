<template>
  <div class="max-w-4xl mx-auto py-16 px-4">
    <h1 class="text-4xl font-bold mb-8 text-green-700">À propos de LIGNO VERT</h1>
    <section class="mb-12">
      <h2 class="text-2xl font-semibold mb-2">Notre histoire</h2>
      <p class="text-lg">Fondée en 2016, LIGNO VERT est une entreprise marocaine spécialisée dans le paysagisme, l'aménagement, la création et l'entretien d'espaces verts extérieurs et intérieurs. Notre expertise va de l'étude technique à l'exécution sur le terrain, avec un souci constant de qualité, durabilité et innovation.</p>
    </section>
    <section class="mb-12">
      <h2 class="text-2xl font-semibold mb-2">Nos valeurs</h2>
      <ul class="grid grid-cols-1 md:grid-cols-2 gap-6">
        <li v-for="(value, i) in valeurs" :key="i" class="flex items-start gap-4 p-4 bg-green-50 rounded-xl shadow">
          <Icon :name="value.icon" class="text-3xl text-green-600" />
          <div>
            <h3 class="font-bold">{{ value.title }}</h3>
            <p class="text-sm">{{ value.desc }}</p>
          </div>
        </li>
      </ul>
    </section>
    <section class="mb-12">
      <h2 class="text-2xl font-semibold mb-2">Vision & Mission</h2>
      <p class="text-lg">LIGNO VERT vise à être un acteur de référence du paysagisme au Maroc, en conjuguant excellence technique, engagement humain et impact positif sur l'environnement et les communautés.</p>
    </section>
    <section>
      <h2 class="text-2xl font-semibold mb-2">Présence nationale</h2>
      <ul class="list-disc ml-8 text-lg">
        <li>Zone Nord-Est</li>
        <li>Zone Centre</li>
        <li>Zone Sud</li>
        <li>Siège à Rabat</li>
      </ul>
    </section>
  </div>
</template>

<script setup lang="ts">
const valeurs = [
  { icon: 'mdi:account-heart', title: "L'humain en premier", desc: "Valorisation des collaborateurs, bien-être et sécurité au travail." },
  { icon: 'mdi:account-group', title: "Travail en équipe", desc: "Synergie et collaboration sur chaque projet." },
  { icon: 'mdi:share-variant', title: "Partage de l'information", desc: "Culture d'amélioration continue par la transmission du savoir." },
  { icon: 'mdi:earth', title: "Communautés élargies", desc: "Acteur de développement local (revendeurs, fournisseurs)." },
  { icon: 'mdi:handshake', title: "Relations fortes", desc: "Relations durables et professionnelles avec les partenaires." }
]
</script> 