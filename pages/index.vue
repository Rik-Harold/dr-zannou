<template>
  <div id="sections">
    <!-- Bannière -->
    <banniere-section />
    <!-- Qui suis-je -->
    <qui-suis-je />
  </div>
</template>

<script>
// Importation des sections de page
import BanniereSection from '@/components/Banniere.vue'
import QuiSuisJe from '@/components/QuiSuisJe.vue'
export default {
  name: 'IndexPage',
  components: {
    BanniereSection,
    QuiSuisJe
  },
  layout: 'main'
}
</script>

<style scoped>
.sections {
  position: relative;
  width: 100%;
  margin: 0;
  padding: 0;
}
</style>
