<template>
  <div class="bg-gradient-to-b from-white via-amber-50 to-lime-50 min-h-screen font-sans">
    <!-- Hero Section -->
    <section class="relative flex flex-col items-center justify-center text-center py-20 md:py-32 bg-[url('https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=1200&q=80')] bg-cover bg-center">
      <div class="absolute inset-0 bg-white/80 backdrop-blur-sm"></div>
      <div class="relative z-10">
        <h1 class="font-serif text-5xl md:text-6xl font-extrabold text-green-900 tracking-wide mb-6">Jardins parfaits</h1>
        <p class="text-lg md:text-xl text-gray-700 mb-8">L'art du paysagisme, l'excellence au naturel</p>
      </div>
      <!-- SVG décoratif -->
      <svg class="absolute bottom-0 left-0 w-32 h-32 text-lime-200 opacity-60" fill="none" viewBox="0 0 100 100"><circle cx="50" cy="50" r="50" fill="currentColor"/></svg>
    </section>

    <!-- Histoire du nom -->
    <section class="max-w-6xl mx-auto py-16 px-4 grid md:grid-cols-2 gap-12 items-center">
      <div>
        <h2 class="font-serif text-4xl font-bold text-green-900 tracking-wide mb-4">L'histoire derrière le nom</h2>
        <p class="text-gray-600 text-lg leading-relaxed">LIGNO VERT incarne notre passion pour la nature et l'aménagement paysager. Notre nom reflète notre engagement à créer des espaces où chaque détail sublime l'environnement et l'harmonie des lieux.</p>
      </div>
      <img src="https://images.unsplash.com/photo-1464983953574-0892a716854b?auto=format&fit=crop&w=800&q=80" alt="Nature" class="w-full rounded-2xl shadow-lg object-cover h-72 md:h-96 transition hover:scale-105 duration-300" />
    </section>

    <!-- Notre philosophie -->
    <section class="max-w-6xl mx-auto py-16 px-4 grid md:grid-cols-2 gap-12 items-center">
      <img src="https://images.unsplash.com/photo-1500534314209-a25ddb2bd429?auto=format&fit=crop&w=800&q=80" alt="Philosophie" class="w-full rounded-2xl shadow-lg object-cover h-72 md:h-96 transition hover:scale-105 duration-300" />
      <div>
        <h2 class="font-serif text-4xl font-bold text-green-900 tracking-wide mb-4">Notre philosophie</h2>
        <p class="text-gray-600 text-lg leading-relaxed">Chaque jardin est une extension de votre personnalité. Nous privilégions l'écoute, la créativité et le respect de l'environnement pour concevoir des aménagements uniques, esthétiques et durables.</p>
      </div>
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