<template>
  <footer class="bg-green-800 text-white py-8 mt-16">
    <div class="max-w-7xl mx-auto flex flex-col md:flex-row justify-between items-center gap-6 px-4">
      <div class="flex items-center gap-2 mb-4 md:mb-0">
        <Icon name="mdi:sprout" class="text-2xl" />
        <span class="font-bold text-lg">LIGNO VERT</span>
      </div>
      <div class="flex gap-6 mb-4 md:mb-0">
        <NuxtLink to="/" class="footer-link">Accueil</NuxtLink>
        <NuxtLink to="/a-propos" class="footer-link">À propos</NuxtLink>
        <NuxtLink to="/services" class="footer-link">Services</NuxtLink>
        <NuxtLink to="/projets" class="footer-link">Projets</NuxtLink>
        <NuxtLink to="/contact" class="footer-link">Contact</NuxtLink>
      </div>
      <div class="flex gap-4">
        <a href="https://facebook.com" target="_blank" rel="noopener" aria-label="Facebook"><Icon name="mdi:facebook" class="text-2xl hover:text-green-300 transition" /></a>
        <a href="https://instagram.com" target="_blank" rel="noopener" aria-label="Instagram"><Icon name="mdi:instagram" class="text-2xl hover:text-green-300 transition" /></a>
        <a href="https://linkedin.com" target="_blank" rel="noopener" aria-label="LinkedIn"><Icon name="mdi:linkedin" class="text-2xl hover:text-green-300 transition" /></a>
      </div>
    </div>
    <div class="text-center text-green-200 text-xs mt-6">© 2016-2024 LIGNO VERT. Tous droits réservés.</div>
  </footer>
</template>

<style scoped>
.footer-link {
  @apply text-white hover:text-green-300 transition;
}
</style> 