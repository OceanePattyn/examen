<template>
    <div class="flex flex-col items-center w-full py-16 bg-white">
      
      <!-- Titre de la section -->
      <h2 class="text-4xl font-bold text-[#24170B] mb-12 leading-[1.7] text-center" style="font-family: 'Playwrite BE WAL', sans-serif;">
        3 options d'apprentissage...
      </h2>
  
      <!-- Conteneur des 3 options -->
      <div class="w-4/5 flex flex-col lg:flex-row justify-between gap-8">
  
        <!-- Option 1 : Formation en groupe -->
        <div class="flex-1 bg-[#997555] text-white rounded-3xl shadow-2xl p-8 text-center flex flex-col items-center justify-center space-y-6">
          <h3 class="text-2xl font-semibold leading-[2]" style="font-family: 'Playwrite BE WAL', sans-serif;">
            Formation en groupe<br>(de 1 à 5 personnes)
          </h3>
          <p class="text-lg leading-relaxed">
            Ces formations se déroulent en soirée de 18h à 21h (ou 22h), ou le samedi après-midi de 14h30 à 17h30/18h30.
            Le principe des formations est que vous puissiez repartir avec les recettes, les produits que vous avez produits ainsi que tous les trucs à astuces pour ne plus jamais rien rater à la maison.
          </p>
        </div>
  
        <!-- Option 2 : Team Building -->
        <div class="flex-1 bg-[#997555] text-white rounded-3xl shadow-2xl p-8 text-center flex flex-col items-center justify-center space-y-6">
          <h3 class="text-2xl font-semibold leading-[2]" style="font-family: 'Playwrite BE WAL', sans-serif;">
            Team Building<br>(jusqu'à 8 personnes)
          </h3>
          <p class="text-lg leading-relaxed">
            Vous cherchez une chouette activité avec vos collègues ? Ces formations en team building seront faites pour vous.
            En 4 heures de temps, vous et vos collègues repartirez avec des pains, baguettes, des croissants, ou autre ! à votre choix.
            Réservation uniquement sur demande et en fonction du nombre de participants !
          </p>
        </div>
  
        <!-- Option 3 : Anniversaires -->
        <div class="flex-1 bg-[#997555] text-white rounded-3xl shadow-2xl p-8 text-center flex flex-col items-center justify-center space-y-6">
          <h3 class="text-2xl font-semibold leading-[2]" style="font-family: 'Playwrite BE WAL', sans-serif;">
            Anniversaires<br>(jusqu'à 8 personnes)
          </h3>
          <p class="text-lg leading-relaxed">
            Vous n’avez pas d’idée pour animer un anniversaire ? Que cela se passe chez vous ou ailleurs, il sera toujours possible d’animer une activité de gâteaux, à déguster tous frais.
            Quoi de plus ludique que d’apprendre à cuisiner des bonnes choses tout en ayant ses amis autour de vous !
            Réservation uniquement sur demande et en fonction du lieu ainsi que du nombre de participants !
          </p>
        </div>
  
      </div>
  
      <!-- 9 Options d'Ateliers -->
      <h2 class="text-4xl font-bold text-[#24170B] mb-12 leading-[1.7] text-center mt-16" style="font-family: 'Playwrite BE WAL', sans-serif;">
        Toutes les formations ...
      </h2>
  
      <!-- Conteneur des 9 options -->
      <div class="w-4/5 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div v-for="(atelier, index) in ateliers" :key="index" class="bg-[#997555] text-white rounded-3xl shadow-2xl p-8 text-center flex flex-col items-center justify-between space-y-6">
          
          <!-- Image ronde -->
          <div class="w-24 h-24 md:w-28 md:h-28 rounded-full overflow-hidden border-4 border-white shadow-lg mb-4">
            <img :src="atelier.image" :alt="atelier.titre" class="w-full h-full object-cover">
          </div>
  
          <!-- Titre -->
          <h3 class="text-2xl font-semibold leading-[2]" style="font-family: 'Playwrite BE WAL', sans-serif;">
            {{ atelier.titre }}
          </h3>
  
          <!-- Description -->
          <p class="text-lg leading-relaxed mb-auto">
            {{ atelier.description }}
          </p>
  
          <!-- Prix -->
          <p class="text-xl font-bold mt-auto bg-white text-[#5C3B1E] px-4 py-2 rounded-full">
            {{ atelier.prix }}
          </p>
        </div>
      </div>
  
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        ateliers: [
          {
            titre: "Les viennoiseries",
            image: "/viennoiserie.png",
            description: "Apprenez à faire vos pains au chocolat, croissant, couques suisses, baulus maison. Pour un dimanche tout en douceur, sans jamais sortir de son lit!",
            prix: "69€/4h"
          },
          {
            titre: "Les macarons",
            image: "/macaron.png",
            description: "Envie de faire plaisir ou de se faire plaisir ? Venez découvrir comment faire ses macarons maison, au chocolat, au beurre salé et aux fruits.",
            prix: "69€/3h"
          },
          {
            titre: "La pâte à choux",
            image: "/pate.png",
            description: "Ici, deux produits en 1 : la pâte à chou et la crème pâtissière. Pour des goûters réussis, une petite douceur à refaire à la maison en boucle!",
            prix: "69€/3h"
          },
          {
            titre: "Les tartes aux fruits",
            image: "/tarte.png",
            description: "Réalisez vos tartes aux fruits maison : fraises, multifruits, pommes, sucre, tout cela avec une belle pâte levée sucrée!",
            prix: "69€/3h"
          },
          {
            titre: "La frangipane",
            image: "/frangipane.png",
            description: "La frangipane est à l’honneur. Dans la galette des rois, ou dans une bonne tarte aux myrtilles. Que demander de plus? ",
            prix: "69€/3h"
          },
          {
            titre: "Les goûters des enfants",
            image: "/gouter.png",
            description: "Vous en avez marre d’acheter des biscuits remplis de sucre de l’industrie? Venez apprendre à faire vos mélocakes, rouleaux à la confiture, gaufres maison.",
            prix: "69€/3h"
          },
          {
            titre: "Les pains, brioches, bun's",
            image: "/pain.png",
            description: "Vous désirez faire votre pain maison et déguster vos propres brioches les dimanches matins ? Toutes les techniques n’auront plus de secrets pour vous!",
            prix: "73€/3h-4h"
          },
          {
            titre: "Les javanais, crèmes au beurre, ganaches",
            image: "/javanais.png",
            description: "Vous voulez fêter un anniversaire? C’est vous qui apportez le gâteau ? Dorénavant, ce ne sera plus une tâche complexe, et on vous en redemandera encore!",
            prix: "69€/3h"
          },
          {
            titre: "Les bûches",
            image: "/buches.png",
            description: "Noël approche ? Plus la peine de se précipier dans une boulangerie pour commander sa bûche. Aujourd’hui, on vous apprendra les glaçages, les bavarois aux fruits et chocolats! Miam!",
            prix: "79€/4h"
          }
        ]
      }
    }
  }
  </script>
  
  <style>
  @import url('https://fonts.googleapis.com/css2?family=Playwrite+BE+WAL:wght@100..400&display=swap');
  </style>
  