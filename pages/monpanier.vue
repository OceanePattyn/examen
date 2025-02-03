<template>
    <div class="container mx-auto py-12">
      <div class="flex justify-center items-center">
        <div class="w-full max-w-md p-6 bg-white shadow-md rounded-lg">
          <h1 class="text-3xl font-semibold text-[#24170B] mb-6">Votre Panier</h1>
          <div class="text-center">
            <p class="text-[#24170B] text-lg mb-4">Il n'y a rien dans votre panier pour le moment.</p>
            <p class="text-[#997555] text-sm">Explorez nos ateliers de pâtisserie et ajoutez-en à votre panier pour réserver votre place !</p>
          </div>
          <div class="mt-6 flex justify-center">
            <button @click="redirectToAteliers" class="px-4 py-2 bg-[#997555] text-white rounded-md hover:bg-[#7c5f3d]">
              Voir les ateliers
            </button>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      redirectToAteliers() {
        this.$router.push('/ateliers'); // Remplacer par la page qui affiche les ateliers
      }
    }
  };
  </script>
  
  <style scoped>
  .container {
    max-width: 600px;
  }
  </style>
  