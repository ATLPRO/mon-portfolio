<script setup>
import { ref } from 'vue';

// Création des références réactives pour chaque champ du formulaire
const name = ref('');
const email = ref('');
const message = ref('');

// Fonction pour gérer la soumission du formulaire
const handleSubmit = () => {
  // Ici, vous pouvez gérer l'envoi des données, par exemple à une API
  console.log('Formulaire soumis !');
  console.log('Nom:', name.value);
  console.log('Email:', email.value);
  console.log('Message:', message.value);

  // Remarque : Pour un vrai projet, vous feriez une requête HTTP
  // comme une requête POST avec `fetch` ou `axios`.

  // Réinitialisation des champs après soumission (optionnel)
  name.value = '';
  email.value = '';
  message.value = '';
};
</script>

<template>
     <div  id="projets">
    <h2 class="text-highlight-1 section-title"> Me contacter</h2>
     </div>
  <form @submit.prevent="handleSubmit" class="contact-form">
    <div class="form-group">
      <input type="text" id="name" v-model="name" placeholder="Nom" required>
    </div>
    <div class="form-group">
      <input type="email" id="email" v-model="email" placeholder="Email" required>
    </div>
    <div class="form-group">
      <textarea id="message" v-model="message" rows="5" placeholder="Message" required></textarea>
    </div>
    <button type="submit">Envoyer</button>
  </form>
</template>

<style scoped>
.contact-form {
  max-width: 500px;
  margin: 2em auto;
  padding: 2em;
  border: 1px solid #ccc;
  border-radius: 8px;
  background-color: #f9f9f9;
}

.contact-form h2 {
  text-align: center;
  color: #333;
  margin-bottom: 1.5em;
}

.form-group {
  margin-bottom: 1em;
}

label {
  display: block;
  margin-bottom: 0.5em;
  font-weight: bold;
}

input,
textarea {
  width: 100%;
  padding: 0.8em;
  border: 1px solid #ddd;
  border-radius: 4px;
  box-sizing: border-box;
}

button {
  display: block;
  width: 100%;
  padding: 1em;
  background-color: #42b983; /* La couleur verte de Vue.js */
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  font-size: 1em;
}

button:hover {
  background-color: #349864;
}
</style>