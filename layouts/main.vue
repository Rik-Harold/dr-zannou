<template>
  <v-app>
    <!-- Entête -->
    <nav-barre />
    <v-main>
      <Nuxt />
    </v-main>
    <v-footer
      app
    >
      <footer-section />
    </v-footer>
  </v-app>
</template>

<script>
// Importation des composants nécessaires à la formation du layout
import NavBarre from '@/components/NavBarre.vue'
import FooterSection from '@/components/Footer.vue'
export default {
  name: 'MainLayout',
  components: {
    NavBarre,
    FooterSection
  }
}
</script>

<style>
#contenu {
  background-color: #fff;
}
</style>
