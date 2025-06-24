<template>
  <section class="w-full min-h-screen flex flex-col items-center justify-center py-0 md:py-12 bg-white">
    <div class="relative z-10 w-full max-w-5xl mx-auto px-4 py-12">
      <div class="flex justify-center mb-6">
        <img src="/logo-lignovert.png" alt="Logo Ligno Vert" class="w-24 h-24 object-contain" />
      </div>
      <!-- En-tête accrocheur -->
      <div class="text-center mb-12">
        <h1 class="font-serif text-3xl md:text-4xl font-bold text-green-800 mb-4 drop-shadow-lg">Un projet de jardin&nbsp;? Une question&nbsp;? <br class="hidden md:block" /> Parlons-en.</h1>
        <p class="text-lg text-green-900 font-sans">Nous sommes à votre écoute pour concrétiser vos envies paysagères, partout au Maroc.</p>
      </div>
      <!-- Bloc principal -->
      <div class="flex flex-col md:flex-row gap-10 bg-white/80 rounded-3xl shadow-2xl ring-1 ring-green-200/30 border border-lime-200/30 p-6 md:p-10">
        <!-- Formulaire -->
        <form class="flex-1 flex flex-col gap-4">
          <div class="flex flex-col gap-2">
            <label for="name" class="font-serif text-green-800 font-semibold">Nom complet</label>
            <input id="name" type="text" required class="rounded-xl border border-green-200 px-4 py-2 focus:ring-2 focus:ring-green-300 focus:outline-none bg-white/80 transition" placeholder="Votre nom" />
          </div>
          <div class="flex flex-col gap-2">
            <label for="email" class="font-serif text-green-800 font-semibold">Adresse e-mail</label>
            <input id="email" type="email" required class="rounded-xl border border-green-200 px-4 py-2 focus:ring-2 focus:ring-green-300 focus:outline-none bg-white/80 transition" placeholder="votre@email.com" />
          </div>
          <div class="flex flex-col gap-2">
            <label for="phone" class="font-serif text-green-800 font-semibold">Téléphone</label>
            <input id="phone" type="tel" class="rounded-xl border border-green-200 px-4 py-2 focus:ring-2 focus:ring-green-300 focus:outline-none bg-white/80 transition" placeholder="Votre numéro" />
          </div>
          <div class="flex flex-col gap-2">
            <label for="subject" class="font-serif text-green-800 font-semibold">Sujet</label>
            <input id="subject" type="text" class="rounded-xl border border-green-200 px-4 py-2 focus:ring-2 focus:ring-green-300 focus:outline-none bg-white/80 transition" placeholder="Sujet de votre message" />
          </div>
          <div class="flex flex-col gap-2">
            <label for="message" class="font-serif text-green-800 font-semibold">Message</label>
            <textarea id="message" rows="4" required class="rounded-xl border border-green-200 px-4 py-2 focus:ring-2 focus:ring-green-300 focus:outline-none bg-white/80 transition resize-none" placeholder="Votre message..."></textarea>
          </div>
          <button type="submit" class="mt-4 px-8 py-3 bg-green-700 text-white font-bold rounded-full shadow hover:bg-green-800 transition-all duration-200 text-lg self-start">Envoyer</button>
        </form>
        <!-- Infos & carte -->
        <div class="flex-1 flex flex-col gap-6 justify-between">
          <!-- Carte -->
          <div class="w-full rounded-xl shadow-lg overflow-hidden h-[300px] md:h-[400px] border border-green-200">
            <iframe
              src="https://www.google.com/maps?q=34.020882,-6.849813&hl=fr&z=16&output=embed"
              width="100%"
              height="300"
              style="border:0;"
              allowfullscreen=""
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"
              class="block w-full h-[220px] md:h-[300px]"
            ></iframe>
          </div>
        </div>
      </div>
      <!-- Phrase inspirante -->
      <div class="mt-12 text-center">
        <p class="text-xl italic text-green-700 font-serif mb-6">Chez LIGNO VERT, chaque projet est une rencontre.</p>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
// Aucun JS nécessaire pour l'instant
</script> 