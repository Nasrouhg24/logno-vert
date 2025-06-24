<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import Header from '~/components/Header.vue'
import HeaderMobile from '~/components/HeaderMobile.vue'
import Footer from '~/components/Footer.vue'
import FooterMobile from '~/components/FooterMobile.vue'

const isMobile = ref(false)
const checkMobile = () => {
  isMobile.value = window.innerWidth < 768
}
onMounted(() => {
  checkMobile()
  window.addEventListener('resize', checkMobile)
})
onUnmounted(() => {
  window.removeEventListener('resize', checkMobile)
})
</script>

<template>
  <div>
    <component :is="isMobile ? HeaderMobile : Header" />
    <main class="flex-1 pt-20">
      <NuxtPage />
    </main>
    <component :is="isMobile ? FooterMobile : Footer" />
  </div>
</template> 