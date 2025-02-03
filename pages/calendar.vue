<template>
    <div class="flex flex-col items-center w-full py-16 bg-white">
      <!-- Titre de la section -->
      <h2 class="text-4xl font-bold text-[#24170B] mb-8 leading-[1.7] text-center" style="font-family: 'Playwrite BE WAL', sans-serif;">
        Calendrier des Prochains Ateliers
      </h2>
  
      <!-- Mois et Navigation (visible uniquement sur les grands écrans) -->
      <div class="flex justify-between w-full max-w-3xl mb-8 hidden md:flex">
        <button @click="previousMonth" class="text-xl font-semibold text-[#5C3B1E] hover:text-[#4a2e1f]">
          &lt; Précédent
        </button>
        <span class="text-xl font-semibold text-[#24170B]">
          {{ currentMonthName }} {{ currentYear }}
        </span>
        <button @click="nextMonth" class="text-xl font-semibold text-[#5C3B1E] hover:text-[#4a2e1f]">
          Suivant &gt;
        </button>
      </div>
  
      <!-- Calendrier (visible uniquement sur les grands écrans) -->
      <div class="grid grid-cols-7 gap-2 w-full max-w-3xl hidden md:grid">
        <div v-for="(day, index) in weekDays" :key="index" class="text-center font-semibold text-[#5C3B1E]">
          {{ day }}
        </div>
  
        <!-- Génération des jours du mois -->
        <div v-for="day in daysInMonth" :key="day" class="flex flex-col items-center text-white">
          <div v-if="day" 
               :class="{
                 'w-28 rounded-2xl h-28 flex flex-col items-center justify-center text-lg font-semibold cursor-pointer hover:bg-[#5C3B1E] border border-[#5C3B1E]': true,
                 'bg-[#997555]': !getAteliersForDay(day).length,
                 'bg-[#72573f]': getAteliersForDay(day).length,
               }">
            <span class="text-lg">{{ day }}</span>
            <div v-if="getAteliersForDay(day).length > 0" class="mt-2 text-base text-white text-center">
              <span v-for="atelier in getAteliersForDay(day)" :key="atelier.titre">{{ atelier.titre }}</span>
              <div class="mt-2 text-sm">14h - 18h</div> <!-- Heure ajoutée ici -->
            </div>
          </div>
        </div>
      </div>
  
      <!-- Liste des ateliers (visible uniquement sur les petits écrans) -->
      <div class="w-full max-w-3xl flex flex-col items-center mt-8 md:hidden">
        <div v-for="atelier in prochainsAteliers" :key="atelier.date" class="w-[90%] bg-[#72573f] text-white p-4 mb-4 rounded-xl flex justify-between items-center">
          <div class="flex-1">
            <div class="text-lg font-semibold">
              {{ atelier.titre }}
            </div>
          </div>
          <!-- Section droite contenant la date, le jour et l'heure -->
          <div class="text-sm ml-4 text-right">
            <div>{{ getDayOfWeek(atelier.date) }} - {{ atelier.date }}</div> <!-- Jour et Date -->
            <div>14h - 18h</div> <!-- Heure -->
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        currentDate: new Date(),
        prochainsAteliers: [
          {
            titre: "Les viennoiseries",
            date: "2025-02-10",
          },
          {
            titre: "Les macarons",
            date: "2025-02-15",
          },
          {
            titre: "La pâte à choux",
            date: "2025-02-20",
          },
          {
            titre: "Les tartes aux fruits",
            date: "2025-02-25",
          },
          {
            titre: "La frangipane",
            date: "2025-03-05",
          },
        ],
      };
    },
    computed: {
      currentMonthName() {
        return this.currentDate.toLocaleString("fr-FR", { month: "long" });
      },
      currentYear() {
        return this.currentDate.getFullYear();
      },
      weekDays() {
        return ["Lun", "Mar", "Mer", "Jeu", "Ven", "Sam", "Dim"];
      },
      daysInMonth() {
        const firstDayOfMonth = new Date(this.currentDate.getFullYear(), this.currentDate.getMonth(), 1);
        const lastDayOfMonth = new Date(this.currentDate.getFullYear(), this.currentDate.getMonth() + 1, 0);
  
        const days = [];
        const startingDay = firstDayOfMonth.getDay();
        const totalDays = lastDayOfMonth.getDate();
  
        // Remplir les cases avant le premier jour du mois
        for (let i = 0; i < startingDay; i++) {
          days.push(null); // Case vide
        }
  
        // Remplir les jours du mois
        for (let i = 1; i <= totalDays; i++) {
          days.push(i); // Jours du mois
        }
  
        // Ajouter des cases vides pour compléter la grille
        while (days.length % 7 !== 0) {
          days.push(null); // Case vide
        }
  
        return days;
      },
    },
    methods: {
      previousMonth() {
        this.currentDate.setMonth(this.currentDate.getMonth() - 1);
      },
      nextMonth() {
        this.currentDate.setMonth(this.currentDate.getMonth() + 1);
      },
      getAteliersForDay(day) {
        if (!day) return [];
        return this.prochainsAteliers.filter(atelier => {
          const atelierDate = new Date(atelier.date);
          return atelierDate.getDate() === day && atelierDate.getMonth() === this.currentDate.getMonth();
        });
      },
      // Nouvelle méthode pour obtenir le jour de la semaine pour une date
      getDayOfWeek(date) {
        const dayOfWeek = new Date(date).getDay(); // 0: Dim, 1: Lun, 2: Mar, etc.
        const days = ["Dim", "Lun", "Mar", "Mer", "Jeu", "Ven", "Sam"];
        return days[dayOfWeek];
      },
    },
  };
  </script>
  
  <style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Playwrite+BE+WAL:wght@100..400&display=swap');
  </style>
  