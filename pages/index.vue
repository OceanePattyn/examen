<template>
  <div>
    <!-- En-tête d'introduction avec photo -->
    <header class="relative w-full min-h-screen bg-cover bg-center hidden md:block" :style="{ backgroundImage: 'url(/header.png)' }">
      <div class="absolute inset-0"></div>
    </header>

      <div class="flex justify-center items-center text-center w-full py-16">
        <div class="w-4/5 flex flex-wrap md:flex-nowrap bg-[#997555] rounded-3xl shadow-2xl overflow-hidden">
          <!-- Partie gauche : Texte -->
          <div class="w-full md:w-1/2 p-8 flex flex-col justify-center">
            <h2 class="text-4xl font-bold text-white mb-6 leading-[2]" style="font-family: 'Playwrite BE WAL', sans-serif;">
              Découvrez l'univers de nos ateliers !
            </h2>
            <p class="text-lg text-white leading-relaxed mb-6">
              Pour en savoir plus sur notre passion, notre histoire et les secrets qui se cachent derrière nos créations.
            </p>
            <nuxt-link to="/ateliers" class="inline-block px-6 py-3 bg-[#fff4e8] text-[#24170B] rounded-md hover:bg-[#e6d0b9]">
                  À propos
                </nuxt-link>
          </div>

          <!-- Partie droite : Image unique -->
          <div class="w-full md:w-1/2 flex justify-center p-6">
            <img src="/atelier.png" alt="Atelier de cuisine" class="w-full h-auto object-cover rounded-lg shadow-lg"/>
          </div>
        </div>
      </div>


      <!-- Titre avant le slider -->
      <div class="text-center mt-12 hidden md:block">
        <h2 class="text-4xl font-semibold text-[#24170B] font-playwrite">Pour vous projeter</h2>
      </div>

      <!-- Slider d'images -->
      <div class="mt-6 mb-12 relative hidden md:block">
        <swiper
          :modules="[Navigation, Pagination]"
          :slides-per-view="2"
          :space-between="20"
          :loop="true"
          :pagination="{ clickable: true }"
          :navigation="true"
          class="w-full max-w-4xl mx-auto rounded-lg custom-swiper"
        >
          <swiper-slide v-for="(image, index) in images" :key="index" class="flex justify-center">
            <img :src="image" class="w-full h-96 object-cover rounded-lg"/>
          </swiper-slide>
        </swiper>
      </div>

      <div class="flex justify-center items-center text-center w-full py-16">
        <div class="w-4/5 flex flex-wrap md:flex-nowrap bg-[#997555] rounded-3xl shadow-2xl overflow-hidden">
          <!-- Partie gauche : Texte -->
          <div class="w-full md:w-1/2 flex justify-center p-6">
            <img src="/services.png" alt="Atelier de cuisine" class="w-full h-auto object-cover rounded-lg shadow-lg"/>
          </div>

          <div class="w-full md:w-1/2 p-8 flex flex-col justify-center">
            <h2 class="text-4xl font-bold text-white mb-6 leading-[2]" style="font-family: 'Playwrite BE WAL', sans-serif;">
              Découvrez nos services
            </h2>
            <p class="text-lg text-white leading-relaxed mb-6">
              Explorez nos propositions de services et apprenez l’art de la pâtisserie et de la boulangerie avec une experte. En savoir plus sur nos offres et réservez votre place dès aujourd’hui !
            </p>
            <nuxt-link to="/services" class="inline-block px-6 py-3 bg-[#fff4e8] text-[#24170B] rounded-md hover:bg-[#e6d0b9]">
              Services
            </nuxt-link>
          </div>
        </div>
      </div>

      <!-- NOUVELLE SECTION : Texte à gauche, boutons à droite -->
      <div class="container mx-auto py-12 px-4">
        <div class="flex flex-wrap md:flex-nowrap items-stretch">
          <div class="w-full md:w-2/5 bg-[#997555] text-center text-white p-6 flex flex-col justify-center rounded-lg">
            <h2 class="text-3xl font-semibold text-white mb-4 font-playwrite">Accéder à nos ateliers</h2>
            <p class="text-lg text-white">
              Pour nous rendre visite, consultez les détails du parking et de l’adresse ici. Nous avons hâte de vous accueillir !
            </p>
          </div>
          <div class="w-full md:w-3/5 flex flex-col">
            <a 
            href="https://www.google.com/maps?q=22+Rue+des+Gen%C3%AAts,+1390+Grez-Doiceau,+Belgique" 
            target="_blank"
            class="flex-1 bg-[#e6d0b9] text-[#24170B] text-center flex items-center justify-center text-xl font-semibold p-6 rounded-lg hover:bg-[#c4a386]"
          >
            📍 Adresse
          </a>
          <a 
            href="https://www.google.com/maps?q=Rue+des+Merisiers,+1390+Grez-Doiceau,+Belgique" 
            target="_blank"
            class="flex-1 bg-[#e6d0b9] text-[#24170B] text-center flex items-center justify-center text-xl font-semibold p-6 rounded-lg mt-2 hover:bg-[#c4a386]"
          >
            🚗 Parking
          </a>
          </div>
        </div>
      </div>

   
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Navigation, Pagination } from "swiper/modules";
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    const images = [
      "/image1.jpg",
      "/image2.jpg",
      "/image3.jpg",
      "/image4.jpg"
    ];
    return { images, Navigation, Pagination };
  }
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Playwrite+BE+WAL:wght@100..400&display=swap');

img {
  max-width: 100%;
  height: auto;
}

/* Personnalisation de la pagination */
.custom-swiper :deep(.swiper-pagination-bullet) {
  background: #997555; /* Marron clair */
  opacity: 0.5;
}

.custom-swiper :deep(.swiper-pagination-bullet-active) {
  background: #24170B; /* Marron foncé */
  opacity: 1;
}

/* Personnalisation des flèches */
.custom-swiper :deep(.swiper-button-next),
.custom-swiper :deep(.swiper-button-prev) {
  color: #997555; /* Marron clair */
  transition: color 0.3s ease-in-out;
}

.custom-swiper :deep(.swiper-button-next):hover,
.custom-swiper :deep(.swiper-button-prev):hover {
  color: #24170B; /* Marron foncé */
}

.custom-swiper img {
  display: block;
  margin: 0 auto;
  height: 40% !important; /* Ajuste selon tes besoins */
  width: 70% !important; /* Ajuste selon tes besoins */
  object-fit: cover;
}


/* Applique la police Playwrite aux titres et augmente l'interligne */
h2 {
  font-family: 'Playwrite BE WAL', sans-serif;
  line-height: 1.7; /* Interligne plus grand */
}


</style>

