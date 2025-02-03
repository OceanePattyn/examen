<template>
  <div class="flex flex-col items-center w-full">
    
    <!-- Section Geneviève -->
    <div class="min-h-screen flex justify-center items-center w-full py-16">
      <div class="w-4/5 bg-[#FFF4E8] rounded-3xl shadow-2xl overflow-hidden">
        <!-- Partie supérieure -->
        <div class="relative flex justify-center items-center h-[30vh]">
          <div class="absolute top-1/2 transform -translate-y-1/2 w-40 h-40 md:w-52 md:h-52 rounded-full overflow-hidden border-4 border-[#997555] shadow-lg">
            <img src="/genevieve.png" alt="Geneviève Van Damme" class="w-full h-full object-cover">
          </div>
        </div>

        <!-- Partie inférieure -->
        <div class="bg-[#997555] flex flex-col items-center text-center text-white py-16 px-6 h-auto rounded-b-3xl">
          <h1 class="text-5xl font-bold mb-6 leading-[2]" style="font-family: 'Playwrite BE WAL', sans-serif;">
            Geneviève
          </h1>
          <p class="text-lg max-w-2xl leading-relaxed">
            Après 4 années d’études en boulangerie-pâtisserie et une réorientation professionnelle, je souhaite vous faire acquérir les secrets pour réussir vos pains, et pâtisseries maison.
            J’ai travaillé pendant 2 années et demi en boulangerie et perfectionné mon savoir-faire. 
            Je suis passionnée par le fait de transmettre un savoir-faire et par la bonne cuisine, le tout “fait maison”. 
            Ça a tellement plus de charme et de goût !
          </p>
          <p class="text-xl font-semibold mt-6" style="font-family: 'Playwrite BE WAL', sans-serif;">
            Fondatrice de L'atelier "Fait maison"
          </p>
        </div>
      </div>
    </div>

    <!-- Section La passion de cuisiner -->
    <div class="flex justify-center items-center text-center w-full py-16">
      <div class="w-4/5 flex flex-wrap md:flex-nowrap bg-[#FFF4E8] rounded-3xl shadow-2xl overflow-hidden">
        <!-- Partie gauche : Texte -->
        <div class="w-full md:w-1/2 p-8 flex flex-col justify-center">
          <h2 class="text-4xl font-bold text-[#24170B] mb-6 leading-[2]" style="font-family: 'Playwrite BE WAL', sans-serif;">
            La passion de cuisiner
          </h2>
          <p class="text-lg text-[#24170B] leading-relaxed">
            Dans mon atelier, qui ressemble à une cuisine ordinaire, je vous ferai parvenir les trucs et astuces 
            pour réussir comme dans un atelier pro vos produits maison. 
            Les outils sont des robots mixeurs planétaires de 7 litres, que vous pourrez utiliser par groupes de 2 
            pour plus de facilité au niveau des quantités. 
            Tout le matériel est fourni, vous n’aurez qu’à prendre un stylo, une feuille pour réécrire votre recette 
            ainsi qu’un bac solide pour reprendre vos réalisations (un fond plat de préférence, et suffisamment grand et haut pour divers montages).
          </p>
        </div>

        <!-- Partie droite : Images -->
        <div class="w-full md:w-1/2 flex flex-col gap-4 p-6">
          <div class="w-full h-1/2">
            <img src="/cuisine-haut.png" alt="Atelier de cuisine" class="w-full h-full object-cover rounded-lg shadow-lg"/>
          </div>
          <div class="w-full h-1/2">
            <img src="/cuisine-bas.png" alt="Matériel de cuisine" class="w-full h-full object-cover rounded-lg shadow-lg"/>
          </div>
        </div>
      </div>
    </div>

    <!-- Section Pourquoi un tel concept? -->
    <div class="flex justify-center items-center text-center w-full py-16">
      <div class="w-4/5 flex flex-wrap md:flex-nowrap bg-[#997555] rounded-3xl shadow-2xl overflow-hidden">
          <!-- Partie gauche : Images -->
          <div class="w-full md:w-1/2 flex flex-col gap-4 p-6">
              <div class="w-full h-1/2">
                <img src="/concept-haut.png" alt="Atelier de cuisine" class="w-full h-full object-cover rounded-lg shadow-lg"/>
              </div>
              <div class="w-full h-1/2">
                <img src="/concept-bas.png" alt="Matériel de cuisine" class="w-full h-full object-cover rounded-lg shadow-lg"/>
              </div>
            </div>
    
        <!-- Partie droite : Texte -->
        <div class="w-full md:w-1/2 p-8 flex flex-col justify-center">
          <h2 class="text-4xl font-bold text-white mb-6 leading-[2]" style="font-family: 'Playwrite BE WAL', sans-serif;">
            Pourquoi un tel concept ?
          </h2>
          <p class="text-lg text-white leading-relaxed">
            Dans mon atelier, qui ressemble à une cuisine ordinaire, je vous ferai parvenir les trucs et astuces 
            pour réussir comme dans un atelier pro vos produits maison. 
            Les outils sont des robots mixeurs planétaires de 7 litres, que vous pourrez utiliser par groupes de 2 
            pour plus de facilité au niveau des quantités. 
            Tout le matériel est fourni, vous n’aurez qu’à prendre un stylo, une feuille pour réécrire votre recette 
            ainsi qu’un bac solide pour reprendre vos réalisations (un fond plat de préférence, et suffisamment grand et haut pour divers montages).
          </p>
        </div>
      </div>
    </div>

  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Playwrite+BE+WAL:wght@100..400&display=swap');
</style>
