<template>
    <div class="container mx-auto py-8">
      <div class="flex justify-center items-center">
        <!-- Formulaire de Connexion -->
        <div v-if="!isSignup" class="w-full max-w-md p-6 bg-white shadow-md rounded-lg">
          <h1 class="text-2xl font-semibold mb-6">Connexion</h1>
          <form @submit.prevent="handleLogin">
            <div class="mb-4">
              <label for="email" class="block text-sm font-medium text-gray-700">Email</label>
              <input v-model="email" type="email" id="email" required class="w-full p-2 mt-2 border border-gray-300 rounded-md" />
            </div>
            <div class="mb-4">
              <label for="password" class="block text-sm font-medium text-gray-700">Mot de passe</label>
              <input v-model="password" type="password" id="password" required class="w-full p-2 mt-2 border border-gray-300 rounded-md" />
            </div>
            <button type="submit" class="w-full p-2 bg-[#997555] text-white rounded-md hover:bg-[#997555]">Se connecter</button>
          </form>
          <p class="text-sm mt-4 text-center">
            Pas encore de compte ?
            <a href="#" @click="toggleForm" class="text-[#997555] hover:text-[#997555]">Inscrivez-vous ici</a>
          </p>
        </div>
  
        <!-- Formulaire d'Inscription -->
        <div v-else class="w-full max-w-md p-6 bg-white shadow-md rounded-lg">
          <h1 class="text-2xl font-semibold mb-6">S'inscrire</h1>
          <form @submit.prevent="handleSignup">
            <div class="mb-4">
              <label for="fullname" class="block text-sm font-medium text-gray-700">Nom complet</label>
              <input v-model="fullname" type="text" id="fullname" required class="w-full p-2 mt-2 border border-gray-300 rounded-md" />
            </div>
            <div class="mb-4">
              <label for="email" class="block text-sm font-medium text-gray-700">Email</label>
              <input v-model="email" type="email" id="email" required class="w-full p-2 mt-2 border border-gray-300 rounded-md" />
            </div>
            <div class="mb-4">
              <label for="password" class="block text-sm font-medium text-gray-700">Mot de passe</label>
              <input v-model="password" type="password" id="password" required class="w-full p-2 mt-2 border border-gray-300 rounded-md" />
            </div>
            <button type="submit" class="w-full p-2 bg-[#997555] text-white rounded-md hover:bg-[#997555]">S'inscrire</button>
          </form>
          <p class="text-sm mt-4 text-center">
            Vous avez déjà un compte ?
            <a href="#" @click="toggleForm" class="text-[#997555] hover:text-[#997555]">Connectez-vous ici</a>
          </p>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        isSignup: false, // Gère si on est en mode "Inscription" ou "Connexion"
        fullname: '',
        email: '',
        password: '',
      };
    },
    methods: {
      toggleForm() {
        this.isSignup = !this.isSignup; // Change entre connexion et inscription
      },
      handleLogin() {
        console.log('Tentative de connexion avec', this.email, this.password);
        // Simule une connexion réussie
        alert('Connexion réussie (factice)');
      },
      handleSignup() {
        console.log('Tentative d\'inscription avec', this.fullname, this.email, this.password);
        // Simule une inscription réussie
        alert('Inscription réussie (factice)');
      },
    },
  };
  </script>
  
  <style scoped>
  .container {
    max-width: 600px;
  }
  </style>
  