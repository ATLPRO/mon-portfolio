<script setup>
import { ref } from 'vue';

const showMenu = ref(false);

const toggleMenu = () => {
  showMenu.value = !showMenu.value;
};
</script>

<template>
  <nav class="top-navbar">
    <div class="logo">
      <a href="#accueil">Léa AGUEDE</a>
    </div>
    <button class="hamburger" @click="toggleMenu" aria-label="Toggle navigation menu">
      <span class="bar"></span>
      <span class="bar"></span>
      <span class="bar"></span>
    </button>
    <ul class="nav-links" :class="{ 'is-active': showMenu }">
      <li><a href="#a-propos" @click="toggleMenu">A propos</a></li>
      <li><a href="#mes-technos" @click="toggleMenu">Mes technos</a></li>
      <li><a href="#experiences" @click="toggleMenu">Expériences</a></li>
      <li><a href="#projets" @click="toggleMenu">Projets</a></li>
      <li><a href="#contact" @click="toggleMenu">Contact</a></li>
    </ul>
  </nav>
</template>

<style scoped>
.top-navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #2c3e50;
  padding: 1rem 2rem;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
  position: sticky;
  top: 0;
  z-index: 1000;
}

.logo a {
  color: white;
  text-decoration: none;
  font-size: 1.5rem;
  font-weight: bold;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 2rem;
  margin: 0;
  padding: 0;
}

.nav-links li a {
  color: white;
  text-decoration: none;
  font-size: 1rem;
  transition: color 0.3s ease;
}

.nav-links li a:hover {
  color: #42b983;
}

.hamburger {
  display: none;
  background: none;
  border: none;
  cursor: pointer;
  padding: 0;
}

.hamburger .bar {
  display: block;
  width: 25px;
  height: 3px;
  background-color: white;
  margin: 5px auto;
  transition: all 0.3s ease-in-out;
}

/* Styles pour le mode mobile */
@media (max-width: 768px) {
  .nav-links {
    position: fixed;
    top: 60px;
    left: 0;
    width: 100%;
    height: calc(100vh - 60px); /* Ajuste la hauteur pour le viewport */
    flex-direction: column;
    background-color: #2c3e50;
    text-align: center;
    padding: 20px 0;
    transform: translateX(100%);
    transition: transform 0.3s ease-in-out;
  }

  .nav-links.is-active {
    transform: translateX(0);
  }

  .nav-links li {
    margin: 15px 0;
  }

  .hamburger {
    display: block;
  }

  /* Animation du bouton hamburger */
  .hamburger.is-active .bar:nth-child(2) {
    opacity: 0;
  }

  .hamburger.is-active .bar:nth-child(1) {
    transform: translateY(8px) rotate(45deg);
  }

  .hamburger.is-active .bar:nth-child(3) {
    transform: translateY(-8px) rotate(-45deg);
  }
}
</style>