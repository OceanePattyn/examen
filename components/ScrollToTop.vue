<template>
    <button
      v-if="showButton"
      @click="scrollToTop"
      class="fixed bottom-4 right-4 bg-[#997555] text-white p-4 rounded-full shadow-lg hover:bg-[#70553d] transition-all"
      aria-label="Retour en haut de la page"
    >
      <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-6 h-6">
        <path stroke-linecap="round" stroke-linejoin="round" d="M19 14l-7-7-7 7" />
      </svg>
    </button>
  </template>
  
  <script>
  export default {
    data() {
      return {
        showButton: false,
      };
    },
    methods: {
      scrollToTop() {
        window.scrollTo({ top: 0, behavior: 'smooth' });
      },
      handleScroll() {
        this.showButton = window.scrollY > 200; // Affiche le bouton après avoir défilé de 200px
      },
    },
    mounted() {
      window.addEventListener('scroll', this.handleScroll);
    },
    destroyed() {
      window.removeEventListener('scroll', this.handleScroll);
    },
  };
  </script>
  
  <style scoped>
  button {
    z-index: 999;
  }
  </style>
  