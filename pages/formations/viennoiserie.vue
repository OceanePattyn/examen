<template>
    <div class="container mx-auto px-4 py-12">
      <!-- Section Produit -->
      <div class="flex flex-col lg:flex-row gap-8">
        <!-- Image du produit -->
        <div class="w-full lg:w-1/2">
          <img :src="product.image" :alt="product.title" class="w-full h-auto rounded-lg shadow-lg"/>
        </div>
        
        <!-- Détails du produit -->
        <div class="w-full lg:w-1/2">
            <h1 class="text-4xl font-bold mb-6 leading-[2]" style="font-family: 'Playwrite BE WAL', sans-serif;">{{ product.title }}</h1>
          <p class="text-lg text-gray-700 mb-4">{{ product.shortDescription }}</p>
  
          <!-- Sélection de la date -->
          <div class="mb-4">
            <label for="date" class="block text-sm font-medium text-gray-700">Choisir une date</label>
            <select id="date" v-model="selectedDate" class="w-full p-2 border rounded-md text-gray-700">
              <option v-for="(date, index) in product.dates" :key="index" :value="date">{{ date }}</option>
            </select>
          </div>
  
          <!-- Prix -->
          <p class="text-xl font-bold text-[#997555] mb-4">{{ product.price }} €</p>
  
          <!-- Bouton d'achat -->
          <button class="bg-[#997555] text-white py-2 px-4 rounded-lg w-full mt-4 cursor-not-allowed" disabled>
            Ajouter au panier
          </button>
        </div>
      </div>
  
      <!-- Produits similaires -->
      <div class="mt-12">
        <h2 class="text-2xl font-semibold text-[#24170B] mb-6">Produits similaires</h2>
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
          <div v-for="(similarProduct, index) in similarProducts" :key="index" class="bg-[#997555] rounded-lg overflow-hidden shadow-lg">
            <nuxt-link :to="similarProduct.link" class="block">
              <img :src="similarProduct.image" :alt="similarProduct.title" class="w-full h-48 object-cover"/>
              <div class="p-4 text-center">
                <h3 class="text-lg font-semibold text-white">{{ similarProduct.title }}</h3>
                <p class="text-white text-lg">{{ similarProduct.price }} €</p>
              </div>
            </nuxt-link>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        selectedDate: '',
        product: {
          title: 'Viennoiseries',
          shortDescription: 'Apprenez à réaliser des viennoiseries artisanales avec cette formation complète.',
          image: '/31236.jpg',
          price: 69,
          dates: ['Mardi 10 Février de 14h à 18h'],
        },
        similarProducts: [
          {
            title: 'Macarons',
            image: '/2150714617.jpg',
            price: 69,
            link: '/formations/macaron',
          },
          {
            title: 'Pâte à choux',
            image: '/91563.jpg',
            price: 69,
            link: '/formations/pate',
          },
          {
            title: 'Tarte aux fruits',
            image: '/24364.jpg',
            price: 69,
            link: '/formations/tarte',
          },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  h2, h3, p {
    font-family: 'Playwrite', sans-serif;
  }
  </style>
  