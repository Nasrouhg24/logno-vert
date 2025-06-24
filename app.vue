<script setup lang="ts">
import Header from '~/components/Header.vue'
import Footer from '~/components/Footer.vue'
</script>

<template>
  <div>
    <Head>
      <link href="https://cdn.jsdelivr.net/npm/tailwindcss@3.4.1/dist/tailwind.min.css" rel="stylesheet">
    </Head>
    <div class="min-h-screen bg-gradient-to-b from-green-50 to-white flex flex-col">
      <Header />
      <main class="flex-1 pt-20">
        <NuxtPage />
      </main>
      <Footer />
    </div>
  </div>
</template>
