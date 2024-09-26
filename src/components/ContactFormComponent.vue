<script setup>
import { ref } from 'vue';

const formData = ref({
  name: '',
  email: '',
  message: ''
});

const submittedData = ref({});

const handleSubmit = () => {

  submittedData.value = { ...formData.value };
  }
</script>

<template>
  <div class="flex flex-col justify-center items-center min-h-screen bg-gray-50">
    <form @submit.prevent="handleSubmit" 
      class="bg-white p-8 rounded-lg shadow-md space-y-4 max-w-lg w-full mb-4"
    >
      <!-- Champ Nom -->
      <div>
        <label for="name" class="block text-lg font-medium">Nom</label>
        <input 
          type="text" 
          id="name" 
          v-model="formData.name" 
          class="w-full mt-1 p-2 border border-gray-300 rounded" 
          placeholder="Entrez votre nom"
          required
        />
      </div>

      <!-- Champ E-mail -->
      <div>
        <label for="email" class="block text-lg font-medium">E-mail</label>
        <input 
          type="email" 
          id="email" 
          v-model="formData.email" 
          class="w-full mt-1 p-2 border border-gray-300 rounded" 
          placeholder="Entrez votre e-mail"
          required
        />
      </div>

      <!-- Champ Message -->
      <div>
        <label for="message" class="block text-lg font-medium">Message</label>
        <textarea 
          id="message" 
          v-model="formData.message" 
          class="w-full mt-1 p-2 border border-gray-300 rounded" 
          placeholder="Votre message" 
          rows="4" 
          required
        ></textarea>
      </div>

      <!-- Bouton de soumission -->
      <div>
        <button 
          type="submit" 
          class="w-full bg-blue-500 text-white p-2 rounded hover:bg-blue-600 transition"
        >
          Envoyer
        </button>
      </div>
    </form>
    <div class="bg-white p-8 shadow-md max-w-lg w-full">
      <h3 class="text-xl font-bold mb-4">Valeurs du formulaire :</h3>
      <p><strong>Nom :</strong> {{ submittedData.name }}</p>
      <p><strong>Email :</strong> {{ submittedData.email }}</p>
      <p><strong>Message :</strong> {{ submittedData.message }}</p>
    </div>
  </div>
</template>
