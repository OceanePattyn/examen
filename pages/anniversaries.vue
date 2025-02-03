<template>
    <div class="flex flex-col items-center w-full py-16 bg-white">
      <!-- Titre de la section -->
      <h2 class="text-4xl font-bold text-[#24170B] mb-8 leading-[1.7] text-center" style="font-family: 'Playwrite BE WAL', sans-serif;">
        Réservez votre Anniversaire
      </h2>
  
      <!-- Paragraphe de présentation -->
      <p class="w-4/5 text-lg text-center mb-12 max-w-3xl leading-relaxed">
        Merci de choisir notre atelier pour célébrer votre anniversaire ! Pour finaliser votre réservation, veuillez remplir le formulaire ci-dessous avec les détails de votre demande. Une fois soumis, notre équipe vous contactera par e-mail pour confirmer la réservation, discuter des derniers détails, et vous fournir les instructions de paiement. Nous serons ravis de collaborer avec vous pour organiser une fête d’anniversaire inoubliable, adaptée à vos envies et celles de vos invités. À très bientôt pour une célébration mémorable !
      </p>
  
      <!-- Si le formulaire est soumis -->
      <!-- Si le formulaire est soumis -->
        <div v-if="formSubmitted" class="w-4/5 bg-[#997555] text-white rounded-3xl shadow-2xl p-8 mb-8">
        <h3 class="text-2xl font-semibold mb-4">Votre réservation a bien été envoyée !</h3>
        <p class="text-lg leading-relaxed">
            Merci pour votre demande. Notre équipe vous contactera sous peu par e-mail pour finaliser les détails de votre réservation.
        </p>
        <!-- Attention pour préciser que c'est factice -->
        <p class="text-sm text-red-500 mt-4 italic">
            <strong>Attention :</strong> Cette réservation est factice et ne constitue pas une réservation réelle. C'est un exemple pour la démonstration.
        </p>
        </div>

  
      <!-- Formulaire de réservation -->
      <div v-if="!formSubmitted" class="w-4/5 bg-[#997555] text-white rounded-3xl shadow-2xl p-8">
        <form @submit.prevent="submitForm" class="flex flex-col gap-6">
          <!-- Nom -->
          <div>
            <label for="nom" class="block text-lg font-semibold mb-2">Nom <span class="text-red-500">*</span></label>
            <input id="nom" type="text" class="w-full p-3 rounded-lg text-black" v-model="form.nom" required />
          </div>
  
          <!-- Prénom -->
          <div>
            <label for="prenom" class="block text-lg font-semibold mb-2">Prénom <span class="text-red-500">*</span></label>
            <input id="prenom" type="text" class="w-full p-3 rounded-lg text-black" v-model="form.prenom" required />
          </div>
  
          <!-- Email -->
          <div>
            <label for="email" class="block text-lg font-semibold mb-2">Email <span class="text-red-500">*</span></label>
            <input id="email" type="email" class="w-full p-3 rounded-lg text-black" v-model="form.email" required />
          </div>
  
          <!-- Nombre de personnes -->
          <div>
            <label for="nombre" class="block text-lg font-semibold mb-2">Nombre de personnes <span class="text-red-500">*</span></label>
            <input
              id="nombre"
              type="range"
              min="2"
              max="10"
              step="1"
              v-model="form.nombrePersonnes"
              class="w-full p-3 rounded-lg text-black"
              required
            />
            <div class="flex justify-between">
              <span>2</span>
              <span>10</span>
            </div>
            <div class="mt-2 text-center font-semibold">
              <span>{{ form.nombrePersonnes }} personnes</span>
            </div>
          </div>
  
          <!-- Date de préférence -->
          <div>
            <label for="date" class="block text-lg font-semibold mb-2">Date de préférence <span class="text-red-500">*</span></label>
            <input id="date" type="date" class="w-full p-3 rounded-lg text-black" v-model="form.date" required />
          </div>
  
          <!-- Thème de préférence -->
          <div>
            <label for="theme" class="block text-lg font-semibold mb-2">Thème de préférence <span class="text-red-500">*</span></label>
            <select id="theme" class="w-full p-3 rounded-lg text-black" v-model="form.theme" required>
              <option value="" disabled selected>Choisissez un thème</option>
              <option value="viennoiseries">Les viennoiseries</option>
              <option value="macarons">Les macarons</option>
              <option value="pate">La pâte à choux</option>
              <option value="tarte">Les tartes aux fruits</option>
              <option value="frangipane">La frangipane</option>
              <option value="gouter">Les goûters des enfants</option>
              <option value="pain">Les pains, brioches, bun's</option>
              <option value="javanais">Les javanais, crèmes au beurre, ganaches</option>
              <option value="buches">Les bûches</option>
            </select>
          </div>
  
          <!-- Bouton envoyer -->
          <div class="mt-6">
            <button type="submit" class="w-full p-3 bg-[#5C3B1E] text-white text-lg font-semibold rounded-lg hover:bg-[#4a2e1f] transition">
              Envoyer
            </button>
          </div>
        </form>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        formSubmitted: false,
        form: {
          nom: '',
          prenom: '',
          email: '',
          nombrePersonnes: 2,
          date: '',
          theme: '',
        },
      };
    },
    methods: {
      submitForm() {
        // Simuler l'envoi du formulaire (normalement ici vous feriez une requête pour soumettre les données)
        this.formSubmitted = true;
        // Reset le formulaire après soumission
        setTimeout(() => {
          this.formSubmitted = false;
          this.form = {
            nom: '',
            prenom: '',
            email: '',
            nombrePersonnes: 2,
            date: '',
            theme: '',
          };
        }, 7000); // Réinitialiser après 7 secondes pour l'exemple
      },
    },
  };
  </script>
  
  <style>
  @import url('https://fonts.googleapis.com/css2?family=Playwrite+BE+WAL:wght@100..400&display=swap');
  </style>
  