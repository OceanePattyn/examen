<template>
  <div>
    <Navbar />
    <NuxtPage />
    <Footer />
    <ScrollToTop /> <!-- Ajout du composant ScrollToTop ici -->
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import ScrollToTop from "@/components/ScrollToTop.vue"; // Importation du composant ScrollToTop

export default {
  components: {
    Navbar,
    ScrollToTop, // Déclaration du composant dans App.vue
  },
};
</script>

<style>
/* Style global si nécessaire */
</style>
