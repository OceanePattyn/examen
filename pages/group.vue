<template>
    <div class="container mx-auto px-4 py-12">
        <h1 class="text-4xl font-bold mb-6 leading-[3] text-center" style="font-family: 'Playwrite BE WAL', sans-serif;">
            Formations en groupe
          </h1>
      
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
        <div v-for="(formation, index) in formations" :key="index" 
             class="bg-[#997555] shadow-lg rounded-xl overflow-hidden border border-[#6D4C41] transition duration-300 hover:bg-[#856040]">
          <nuxt-link :to="formation.link" class="block">
            <img :src="formation.image" :alt="formation.title" 
                 class="w-full h-56 object-cover" />
            <div class="p-4 text-center">
              <h2 class="text-xl font-semibold text-white">{{ formation.title }}</h2>
              <p class="text-white text-lg mt-2">{{ formation.price }} €</p>
            </div>
          </nuxt-link>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    setup() {
      const formations = [
        {
          title: "Viennoiseries",
          image: "/31236.jpg",
          price: "69",
          link: "/formations/viennoiserie",
        },
        {
          title: "Macarons",
          image: "/2150714617.jpg",
          price: "69",
          link: "/formations/macaron",
        },
        {
          title: "Pâte à choux",
          image: "/91563.jpg",
          price: "69",
          link: "/formations/pate",
        },
        {
          title: "Tarte aux fruits",
          image: "/24364.jpg",
          price: "69",
          link: "/formations/tarte",
        },
      ];
      return { formations };
    },
  };
  </script>
  
  <style scoped>
@import url('https://fonts.googleapis.com/css2?family=Playwrite&display=swap'); /* ou le chemin de ton fichier local */
</style>
  
