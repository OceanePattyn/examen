<template>
    <div class="flex flex-col items-center w-full py-16 bg-white">
      <!-- Titre principal -->
      <h2 class="text-4xl leading-[2] font-bold text-[#24170B] mb-8 text-center w-4/5" style="font-family: 'Playwrite BE WAL', sans-serif;">
        Arriver à l'atelier
      </h2>
      
      <!-- Introduction -->
      <p class="text-lg text-[#5C3B1E] text-center max-w-3xl mb-8 w-4/5">
        L'atelier est situé à Grez-Doiceau, un charmant village accessible en voiture, en train ou en bus. Voici comment y accéder facilement.
      </p>
      
      <!-- Google Maps - Adresse de l'atelier -->
      <div class="w-4/5 h-80 mb-12">
        <iframe
          class="w-full h-full rounded-2xl shadow-lg"
          frameborder="0"
          style="border:0"
          allowfullscreen=""
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
          :src="atelierMapUrl">
        </iframe>
      </div>
      
      <!-- Comment y accéder -->
      <h3 class="text-3xl leading-[2] font-semibold text-[#24170B] mb-4 text-center w-4/5" style="font-family: 'Playwrite BE WAL', sans-serif;">
        Comment y accéder ?
      </h3>
      <p class="text-lg text-[#5C3B1E] text-center max-w-3xl mb-12 w-4/5">
        - <strong>En voiture :</strong> L'atelier est accessible via la N25, sortie Grez-Doiceau.<br>
        - <strong>En train :</strong> La gare la plus proche est celle de Pécrot, située à environ 10 minutes en voiture.<br>
        - <strong>En bus :</strong> Plusieurs lignes de bus desservent Grez-Doiceau depuis Wavre et Louvain.
      </p>
      
      <!-- Titre secondaire -->
      <h3 class="text-3xl leading-[2] font-semibold text-[#24170B] mb-4 text-center w-4/5" style="font-family: 'Playwrite BE WAL', sans-serif;">
        Où se garer ?
      </h3>
      
      <!-- Introduction au parking -->
      <p class="text-lg text-[#5C3B1E] text-center max-w-3xl mb-8 w-4/5">
        L'atelier dispose d'un parking, mais il est généralement occupé par les habitants des lieux. Nous vous recommandons de vous garer dans la rue des Merisiers, située à quelques minutes à pied.
      </p>
      
      <!-- Google Maps - Parking recommandé -->
      <div class="w-4/5 h-80">
        <iframe
          class="w-full h-full rounded-2xl shadow-lg"
          frameborder="0"
          style="border:0"
          allowfullscreen=""
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
          :src="parkingMapUrl">
        </iframe>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        atelierMapUrl: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2520.571835374619!2d4.680015677206381!3d50.73716317153385!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47c170cdf36c3fdf%3A0x2e8d5293e3d6d9e!2s22%20Rue%20des%20Genets%2C%201390%20Grez-Doiceau%2C%20Belgique!5e0!3m2!1sfr!2sbe!4v1700000000000!5m2!1sfr!2sbe",
        parkingMapUrl: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2520.771265470073!2d4.682845277206211!3d50.73516357153385!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47c170d0c36c3fdf%3A0x3e9d9e8a3e6d9a!2sRue%20des%20Merisiers%2C%201390%20Grez-Doiceau%2C%20Belgique!5e0!3m2!1sfr!2sbe!4v1700000000000!5m2!1sfr!2sbe"
      };
    }
  };
  </script>