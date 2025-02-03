<template>
    <div>
      <!-- Footer -->
      <div class="bg-[#FFF4E8] text-[#24170B] py-6">
        <div class="container mx-auto">
  
          <!-- Informations centrées avant les réseaux sociaux -->
          <div class="flex flex-col items-center mb-4">
            <p class="text-sm font-bold mb-2">Geneviève Van Damme</p>
            <p class="text-sm mb-2"><a href="tel:+32488252840" class="hover:text-gray-800">+32488252840</a></p>
            <p class="text-sm mb-2"><a href="mailto:latelierfaitmaison1@gmail.com" class="hover:text-gray-800">latelierfaitmaison1@gmail.com</a></p>
            <p class="text-sm mb-2">TVA : BE0883.099.777</p>
          </div>
  
          <!-- Réseaux sociaux centrés -->
          <div class="flex justify-center space-x-6 mb-4">
            <!-- Facebook icon -->
            <a href="https://www.facebook.com" target="_blank" class="hover:text-gray-800">
              <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 24 24" stroke="currentColor" class="w-8 h-8">
                <path d="M22 2.003c0-.342-.279-.62-.623-.62H2.623A.623.623 0 0 0 2 2.003v19.994a.623.623 0 0 0 .623.62h18.754a.623.623 0 0 0 .623-.62V2.003zM12 15.32h-2.118v6.447H7.236v-6.447H5.61V9.325h1.626V7.56c0-2.532 1.478-4.006 4.055-4.006 1.18 0 2.268.086 2.56.125v2.615h-1.822c-1.456 0-1.83.692-1.83 1.742v2.387h3.322l-.434 6.445h-2.888V15.32z"/>
              </svg>
            </a>
          </div>
  
          <!-- Liens - Version mobile: empilés et version desktop: alignés horizontalement -->
          <div class="flex justify-center space-x-6 sm:flex-row sm:space-x-6 sm:space-y-0 sm:mt-4 sm:mb-4 flex-col sm:flex-nowrap sm:items-center sm:space-y-2">
            <nuxt-link to="/politique" class="text-sm hover:text-gray-800">Politique de confidentialité</nuxt-link>
            <nuxt-link to="/mentions-legales" class="text-sm hover:text-gray-800">Mentions légales</nuxt-link>
            <nuxt-link to="/conditions-generales-vente" class="text-sm hover:text-gray-800">Conditions Générales de Vente</nuxt-link>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  
  
  <script>
  export default {
    name: "Footer",
  };
  </script>
  
  <style scoped>
  /* Centrage des icônes sociales */
  .flex {
    justify-content: center;
  }
  
  a {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  a:hover {
    color: #24170B;
  }
  </style>
  