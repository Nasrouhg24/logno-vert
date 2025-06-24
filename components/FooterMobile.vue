<template>
  <footer class="bg-green-950 text-green-100 py-6 px-4 text-center">
    <img src="/logo-lignovert.png" alt="Logo Ligno Vert" class="w-12 h-12 mx-auto mb-2" />
    <nav class="flex flex-col gap-2 mb-4">
      <NuxtLink to="/" class="text-xs text-green-100 hover:text-yellow-500 transition">Accueil</NuxtLink>
      <NuxtLink to="/projets" class="text-xs text-green-100 hover:text-yellow-500 transition">Projets</NuxtLink>
      <NuxtLink to="/services" class="text-xs text-green-100 hover:text-yellow-500 transition">Services</NuxtLink>
      <NuxtLink to="/contact" class="text-xs text-green-100 hover:text-yellow-500 transition">Contact</NuxtLink>
    </nav>
    <div class="flex justify-center gap-3 mb-3">
      <a href="https://www.facebook.com/p/Ligno-Vert-100077596983432/" target="_blank" rel="noopener" aria-label="Facebook" class="w-7 h-7 flex items-center justify-center rounded-full bg-green-800 text-white hover:bg-yellow-600 transition">
        <svg class="w-3.5 h-3.5" fill="currentColor" viewBox="0 0 24 24">
          <path d="M22.675 0h-21.35C.595 0 0 .592 0 1.326v21.348C0 23.408.595 24 1.325 24h11.495v-9.294H9.692v-3.622h3.128V8.413c0-3.1 1.893-4.788 4.659-4.788 1.325 0 2.463.099 2.797.143v3.24l-1.918.001c-1.504 0-1.797.715-1.797 1.763v2.313h3.587l-.467 3.622h-3.12V24h6.116C23.406 24 24 23.408 24 22.674V1.326C24 .592 23.406 0 22.675 0"/>
        </svg>
      </a>
      <a href="https://www.instagram.com/lignovert?igsh=bnh3emViYnN5c3Y=" target="_blank" rel="noopener" aria-label="Instagram" class="w-7 h-7 flex items-center justify-center rounded-full bg-green-800 text-white hover:bg-yellow-600 transition">
        <svg class="w-3.5 h-3.5" fill="currentColor" viewBox="0 0 24 24">
          <path d="M12 2.2c3.2 0 3.584.012 4.85.07 1.17.056 1.97.24 2.43.41a4.92 4.92 0 0 1 1.77 1.01 4.92 4.92 0 0 1 1.01 1.77c.17.46.354 1.26.41 2.43.058 1.266.07 1.65.07 4.85s-.012 3.584-.07 4.85c-.056 1.17-.24 1.97-.41 2.43a4.92 4.92 0 0 1-1.01 1.77 4.92 4.92 0 0 1-1.77 1.01c-.46.17-1.26.354-2.43.41-1.266.058-1.65.07-4.85.07s-3.584-.012-4.85-.07c-1.17-.056-1.97-.24-2.43-.41a4.92 4.92 0 0 1-1.77-1.01 4.92 4.92 0 0 1-1.01-1.77c-.17-.46-.354-1.26-.41-2.43C2.212 15.784 2.2 15.4 2.2 12s.012-3.584.07-4.85c.056-1.17.24-1.97.41-2.43A4.92 4.92 0 0 1 3.69 2.95a4.92 4.92 0 0 1 1.77-1.01c.46-.17 1.26-.354 2.43-.41C8.416 2.212 8.8 2.2 12 2.2zm0-2.2C8.736 0 8.332.012 7.052.07 5.77.128 4.87.312 4.1.54a7.07 7.07 0 0 0-2.56 1.64A7.07 7.07 0 0 0 .54 4.1c-.228.77-.412 1.67-.47 2.952C.012 8.332 0 8.736 0 12c0 3.264.012 3.668.07 4.948.058 1.282.242 2.182.47 2.952a7.07 7.07 0 0 0 1.64 2.56 7.07 7.07 0 0 0 2.56 1.64c.77.228 1.67.412 2.952.47C8.332 23.988 8.736 24 12 24s3.668-.012 4.948-.07c1.282-.058 2.182-.242 2.952-.47a7.07 7.07 0 0 0 2.56-1.64 7.07 7.07 0 0 0 1.64-2.56c.228-.77.412-1.67.47-2.952.058-1.28.07-1.684.07-4.948s-.012-3.668-.07-4.948c-.058-1.282-.242-2.182-.47-2.952a7.07 7.07 0 0 0-1.64-2.56A7.07 7.07 0 0 0 19.9.54c-.77-.228-1.67-.412-2.952-.47C15.668.012 15.264 0 12 0z"/>
          <path d="M12 5.838A6.162 6.162 0 1 0 12 18.162 6.162 6.162 0 1 0 12 5.838zm0 10.162A4 4 0 1 1 12 7.838a4 4 0 0 1 0 8.162zm6.406-11.845a1.44 1.44 0 1 0 0 2.88 1.44 1.44 0 0 0 0-2.88z"/>
        </svg>
      </a>
      <a href="https://ma.linkedin.com/company/ligno-vert" target="_blank" rel="noopener" aria-label="LinkedIn" class="w-7 h-7 flex items-center justify-center rounded-full bg-green-800 text-white hover:bg-yellow-600 transition">
        <svg class="w-3.5 h-3.5" fill="currentColor" viewBox="0 0 24 24">
          <path d="M19 0h-14c-2.76 0-5 2.24-5 5v14c0 2.76 2.24 5 5 5h14c2.76 0 5-2.24 5-5v-14c0-2.76-2.24-5-5-5zm-11.75 20h-3v-10h3v10zm-1.5-11.27c-.97 0-1.75-.79-1.75-1.76s.78-1.76 1.75-1.76 1.75.79 1.75 1.76-.78 1.76-1.75 1.76zm15.25 11.27h-3v-5.6c0-1.34-.03-3.07-1.87-3.07-1.87 0-2.16 1.46-2.16 2.97v5.7h-3v-10h2.89v1.36h.04c.4-.75 1.38-1.54 2.84-1.54 3.04 0 3.6 2 3.6 4.59v5.59z"/>
        </svg>
      </a>
    </div>
    <div class="text-green-100 text-[10px] mt-4">© 2016-2024 LIGNO VERT. Tous droits réservés.</div>
  </footer>
</template> 