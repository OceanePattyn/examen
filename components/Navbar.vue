<template>
  <div>
    <!-- Top Banner -->
    <div class="bg-[#FFF4E8] text-sm py-2 flex justify-between items-center px-4 hidden md:flex">
      <div>
        <a href="/moncompte" class="text-[#24170B] hover:text-gray-800 text-lg">Mon compte</a>
      </div>
      <div class="text-[#24170B] text-center flex items-center space-x-4">
        <div class="flex items-center space-x-2">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
           <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 6.75c0 8.284 6.716 15 15 15h2.25a2.25 2.25 0 0 0 2.25-2.25v-1.372c0-.516-.351-.966-.852-1.091l-4.423-1.106c-.44-.11-.902.055-1.173.417l-.97 1.293c-.282.376-.769.542-1.21.38a12.035 12.035 0 0 1-7.143-7.143c-.162-.441.004-.928.38-1.21l1.293-.97c.363-.271.527-.734.417-1.173L6.963 3.102a1.125 1.125 0 0 0-1.091-.852H4.5A2.25 2.25 0 0 0 2.25 4.5v2.25Z" />
          </svg>
          <a href="tel:+32488252840" class="text-[#24170B] hover:text-gray-800">+32488252840</a>
        </div>
        <div class="flex items-center space-x-2">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
            <path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 0 1-2.25 2.25h-15a2.25 2.25 0 0 1-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0 0 19.5 4.5h-15a2.25 2.25 0 0 0-2.25 2.25m19.5 0v.243a2.25 2.25 0 0 1-1.07 1.916l-7.5 4.615a2.25 2.25 0 0 1-2.36 0L3.32 8.91a2.25 2.25 0 0 1-1.07-1.916V6.75" />
          </svg>
          <a href="mailto:latelierfaitmaison1@gmail.com" class="text-[#24170B] hover:text-gray-800">latelierfaitmaison1@gmail.com</a>
        </div>
      </div>
      <div class="text-[#24170B] text-right text-lg">
        <a href="https://www.google.com/maps?q=22+rue+des+Genets,+Grez-Doiceau,+Belgique" target="_blank" class="hover:text-gray-800">Adresse</a>
      </div>
    </div>

   <!-- Navbar -->
   <nav class="bg-white shadow-md border-b border-black">
      <div class="container mx-auto flex justify-between items-center py-4 px-4">
        <!-- Search Icon (left) -->
        <div class="flex-shrink-0">
          <button aria-label="Rechercher" class="text-[#24170B] hover:text-gray-800">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-6 h-6">
              <path stroke-linecap="round" stroke-linejoin="round" d="M21 21l-4.35-4.35m0 0A7.5 7.5 0 1116.65 5.65a7.5 7.5 0 010 10.7z" />
            </svg>
          </button>
        </div>

        <!-- Logo (center) -->
        <div class="flex flex-col items-center flex-grow">
          <a href="/" aria-label="Retour à l'accueil">
            <img src="public/logo.png" alt="Logo" class="h-24 mb-2" />
          </a>
        </div>

         <!-- Cart Icon (right) - Hidden on mobile -->
         <div class="flex-shrink-0 hidden md:block">
          <a href="/monpanier" aria-label="Panier" class="text-[#24170B] hover:text-gray-800">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
              <path stroke-linecap="round" stroke-linejoin="round" d="M15.75 10.5V6a3.75 3.75 0 1 0-7.5 0v4.5m11.356-1.993 1.263 12c.07.665-.45 1.243-1.119 1.243H4.25a1.125 1.125 0 0 1-1.12-1.243l1.264-12A1.125 1.125 0 0 1 5.513 7.5h12.974c.576 0 1.059.435 1.119 1.007ZM8.625 10.5a.375.375 0 1 1-.75 0 .375.375 0 0 1 .75 0Zm7.5 0a.375.375 0 1 1-.75 0 .375.375 0 0 1 .75 0Z" />
            </svg>
          </a>
        </div>

        <!-- Hamburger Icon (Mobile) -->
        <div class="md:hidden flex-shrink-0">
          <button @click="toggleMenu" aria-label="Menu" class="text-[#24170B] hover:text-gray-800">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-6 h-6">
              <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
            </svg>
          </button>
        </div>
      </div>

      <!-- Desktop Navigation Menu -->
      <div class="hidden md:block bg-white shadow-md">
        <ul class="flex justify-center space-x-6 text-[#24170B] text-lg py-4">
          <li><a href="/about" class="hover:text-gray-800">À propos</a></li>
          <li><a href="/services" class="hover:text-gray-800">Services</a></li>
          <li class="relative group">
            <button class="hover:text-gray-800">Réservation</button>
            <ul class="absolute hidden group-hover:flex flex-col mt-[-1px] bg-white shadow-lg py-2 rounded-lg z-10">
              <li class="flex justify-center items-center"><a href="/group" class="px-4 py-2 hover:bg-gray-100">Formations en groupe</a></li>
              <li class="flex justify-center items-center"><a href="/teambuilding" class="px-4 py-2 hover:bg-gray-100">Team building</a></li>
              <li class="flex justify-center items-center"><a href="/anniversaries" class="px-4 py-2 hover:bg-gray-100">Anniversaires</a></li>
            </ul>
          </li>
          <li><a href="/calendar" class="hover:text-gray-800">Calendrier</a></li>
          <li><a href="/access" class="hover:text-gray-800">Y accéder</a></li>
        </ul>
      </div>
    </nav>


    <!-- Mobile Menu (Toggleable) -->
    <div v-if="isMenuOpen" class="md:hidden bg-white shadow-lg">
      <ul class="flex flex-col items-center text-[#24170B] text-lg">
        <li><a href="/about" class="px-4 py-2 hover:bg-gray-100">À propos</a></li>
        <li><a href="/services" class="px-4 py-2 hover:bg-gray-100">Services</a></li>
        <li class="relative group">
          <button class="px-4 py-2 hover:bg-gray-100">Réservation</button>
          <ul class="absolute hidden group-hover:flex flex-col mt-[-1px] bg-white shadow-lg py-2 rounded-lg">
              <li class="flex justify-center items-center"><a href="/group" class="px-4 py-2 hover:bg-gray-100">Formations en groupe</a></li>
              <li class="flex justify-center items-center"><a href="/teambuilding" class="px-4 py-2 hover:bg-gray-100">Team building</a></li>
              <li class="flex justify-center items-center"><a href="/anniversaries" class="px-4 py-2 hover:bg-gray-100">Anniversaires</a></li>
            </ul>
        </li>
        <li><a href="/calendar" class="px-4 py-2 hover:bg-gray-100">Calendrier</a></li>
        <li><a href="/access" class="px-4 py-2 hover:bg-gray-100">Y accéder</a></li>
        <li><a href="/monpanier" class="px-4 py-2 hover:bg-gray-100">Panier</a></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isMenuOpen: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
  },
};
</script>

<style scoped>
nav ul li {
  position: relative;
}
nav ul li ul {
  display: none;
}
nav ul li:hover ul {
  display: block;
}
</style>

