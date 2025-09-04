<template>
  <footer class="main-footer">
    <div class="footer-content">
      <div class="footer-section about">
        <h3>Léa AGUEDE</h3>
        <p>Développeuse web passionnée par la création d'expériences numériques élégantes et fonctionnelles.</p>
      </div>
      <div class="footer-section social-links">
        <h3>Suivez-moi</h3>
        <ul>
          <li><a href="https://www.linkedin.com/in/lea-aguede/" target="_blank">LinkedIn</a></li>
          <li><a href="https://wa.me/+237683447149" target="_blank">Whatsapp</a></li>
          <li><a href="https://www.facebook.com/lea-aguede/" target="_blank">Facebook</a></li>
        </ul>
      </div>
      <div class="footer-section contact-info">
        <h3>Contact</h3>
        <p>Email: contactlea237@gmail.com</p>
      </div>
    </div>
    <div class="footer-bottom">
      &copy; 2025 Léa AGUEDE | Tous droits réservés.
    </div>
  </footer>
</template>

<style scoped>
.main-footer {
  background-color: #2c3e50;
  color: white;
  padding: 2rem 1rem;
  font-family: Arial, sans-serif;
  border-top: 4px solid #42b983; /* Ligne de couleur pour accentuer */
}

.footer-content {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  text-align: center;
  margin-bottom: 2rem;
}

.footer-section {
  flex: 1;
  padding: 1rem;
  min-width: 200px;
}

.footer-section h3 {
  margin-bottom: 1rem;
  font-size: 1.25rem;
  color: #42b983; /* Couleur d'accent */
}

.footer-section p, .footer-section a {
  font-size: 0.9rem;
  line-height: 1.6;
  color: white;
  text-decoration: none;
}

.footer-section a:hover {
  text-decoration: underline;
}

.footer-section ul {
  list-style: none;
  padding: 0;
}

.footer-section li {
  margin-bottom: 0.5rem;
}

.footer-bottom {
  text-align: center;
  font-size: 0.8rem;
  padding-top: 1rem;
  border-top: 1px solid #4a647e;
}

/* Media query pour les petits écrans */
@media (max-width: 600px) {
  .footer-content {
    flex-direction: column;
    align-items: center;
  }

  .footer-section {
    margin-bottom: 2rem;
  }
}
</style>