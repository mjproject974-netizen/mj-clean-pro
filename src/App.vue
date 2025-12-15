<template>
  <div class="apple">
    <!-- HEADER -->
    <header class="nav">
      <div class="brand">MJ Clean Pro Service</div>
      <nav>
        <a href="#accueil">Accueil</a>
        <a href="#services">Services</a>
        <a href="#tarifs">Tarifs</a>
        <a href="#contact" class="cta">Contact</a>
      </nav>
    </header>

    <main>
      <!-- HERO -->
      <section id="accueil" class="hero">
        <div class="hero-text">
          <h1>La propreté.<br /><span>Version premium.</span></h1>
          <p>
            Mj Clean Pro Service vous offre un service de nettoyage complet, adapté à vos besoins
            spécifiques.
          </p>
        </div>
      </section>

      <!-- VALEURS -->
      <section class="values">
        <div class="value">
          <h3>Simple</h3>
          <p>Tarifs clairs, services transparents.</p>
        </div>
        <div class="value">
          <h3>Humain</h3>
          <p>Une équipe proche de vous.</p>
        </div>
        <div class="value">
          <h3>Efficace</h3>
          <p>Résultat professionnel garanti.</p>
        </div>
      </section>

      <!-- SERVICES -->
      <section id="services" class="apple-cards">
        <div class="card">
          <img src="https://source.unsplash.com/600x600/?cleaning,home" />
          <h3>Nettoyage ponctuel</h3>
          <p>À la demande</p>
        </div>
        <div class="card">
          <img src="https://source.unsplash.com/600x600/?cleaning,office" />
          <h3>Contrat régulier</h3>
          <p>Sérénité à long terme</p>
        </div>
        <div class="card">
          <img src="https://source.unsplash.com/600x600/?elderly,help" />
          <h3>Aide à domicile</h3>
          <p>Assistance quotidienne</p>
        </div>
      </section>

      <!-- TARIFS -->
      <section id="tarifs" class="pricing">
        <h2>Des tarifs horaires simples.</h2>
        <p class="muted">Au plus proche de vos besoins</p>
        <div class="plans">
          <div class="plan">
            <h3>Occasionnel</h3>
            <p class="price">14.75€</p>
            <p>TTC après crédit impôt</p>
            <p>soit 29.50€ TTC sans crédit impôt</p>
          </div>
          <div class="plan highlight">
            <h3>Abonnement</h3>
            <p class="price">20€</p>
            <p>par heure</p>
          </div>
          <div class="plan">
            <h3>Aide à domicile</h3>
            <p class="price">22€</p>
            <p>par heure</p>
          </div>
        </div>
      </section>
      <!-- CONTACT -->
      <section id="contact" class="contact">
        <h2>Contactez MJ Clean.</h2>
        <p>Réponse rapide, devis gratuit.</p>
        <p class="contact-line">📞 Téléphone : à renseigner</p>
        <p class="contact-line">✉ mjclean.proservices29@gmail.com</p>
      </section>

      <!-- CONTACT FORM -->
      <section id="contact" class="contact">
        <h2>Contactez-nous</h2>
        <p>Réponse rapide, devis gratuit.</p>

        <!-- Formulaire -->
        <form class="apple-form" @submit.prevent="sendEmail">
          <div class="input-group">
            <input v-model="form.name" type="text" placeholder="Nom complet" required />
          </div>

          <div class="input-group">
            <input v-model="form.email" type="email" placeholder="Adresse email" required />
          </div>

          <div class="input-group">
            <input v-model="form.phone" type="tel" placeholder="Téléphone" />
          </div>

          <div class="input-group">
            <textarea v-model="form.message" placeholder="Votre message" required></textarea>
          </div>

          <!-- Placeholder reCAPTCHA -->
          <div class="g-recaptcha" data-sitekey="VOTRE_SITE_KEY"></div>

          <button type="submit" :disabled="loading" :class="{ sending: loading }">
            {{ loading ? 'Envoi...' : 'Envoyer le message' }}
          </button>

          <p v-if="success" class="success show">
            ✅ Merci {{ form.name }}, votre message a été envoyé !
          </p>
          <p v-if="error" class="error show">❌ Erreur, veuillez réessayer.</p>
        </form>
      </section>
    </main>

    <footer>© MJ Clean - Tous droits réservés</footer>
  </div>
</template>

<script setup>
import { ref } from 'vue'
//import emailjs from '@emailjs/browser'

const form = ref({
  name: '',
  email: '',
  phone: '',
  message: '',
})

const loading = ref(false)
const success = ref(false)
const error = ref(false)

const sendEmail = () => {
  loading.value = true
  success.value = false
  error.value = false

  // Envoi email au pro
  emailjs
    .send(
      'SERVICE_ID', // remplace par ton Service ID
      'TEMPLATE_ID', // remplace par ton Template ID
      {
        name: form.value.name,
        email: form.value.email,
        phone: form.value.phone,
        message: form.value.message,
      },
      'PUBLIC_KEY', // remplace par ta Public Key
    )
    .then(() => {
      // Email automatique au client
      emailjs.send(
        'SERVICE_ID',
        'RESPONSE_TEMPLATE',
        {
          name: form.value.name,
          email: form.value.email,
        },
        'PUBLIC_KEY',
      )

      success.value = true
      loading.value = false
      form.value = { name: '', email: '', phone: '', message: '' }
    })
    .catch(() => {
      error.value = true
      loading.value = false
    })
}
</script>

<style scoped>
.apple {
  background: #f5f5f7;
  color: #1d1d1f;
  font-family: -apple-system, BlinkMacSystemFont, system-ui;
}

/* HEADER */
.nav {
  position: sticky;
  top: 0;
  background: rgba(255, 255, 255, 0.85);
  backdrop-filter: blur(12px);
  display: flex;
  justify-content: space-between;
  padding: 18px 40px;
  border-bottom: 1px solid #ddd;
}
.nav a {
  text-decoration: none;
  color: black;
  margin-left: 20px;
}
.cta {
  border: 1px solid black;
  padding: 6px 14px;
  border-radius: 99px;
}

/* HERO */
.hero {
  height: 85vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: url('https://source.unsplash.com/1600x900/?clean,minimal,home') center/cover;
}
.hero-text {
  background: rgba(255, 255, 255, 0.85);
  padding: 40px;
  border-radius: 24px;
  text-align: center;
}
.hero h1 {
  font-size: 50px;
}
.hero span {
  color: #0071e3;
}

/* VALUES */
.values {
  display: flex;
  justify-content: center;
  gap: 60px;
  margin: 80px 20px;
}

/* SERVICES */
.apple-cards {
  display: flex;
  justify-content: center;
  gap: 30px;
  margin: 80px 20px;
}
.card {
  background: white;
  width: 260px;
  border-radius: 24px;
  overflow: hidden;
  box-shadow: 0 15px 40px rgba(0, 0, 0, 0.08);
}
.card img {
  width: 100%;
  height: 240px;
  object-fit: cover;
}
.card h3,
.card p {
  padding: 12px 16px;
}

/* PRICING */
.pricing {
  background: white;
  padding: 100px 20px;
  text-align: center;
}
.plans {
  display: flex;
  justify-content: center;
  gap: 30px;
}
.plan {
  background: #f5f5f7;
  padding: 30px;
  border-radius: 22px;
  width: 200px;
}
.highlight {
  background: black;
  color: white;
}
.highlight .price {
  color: #0af;
}
.price {
  font-size: 46px;
  font-weight: bold;
}

/* FORMULAIRE */
.contact {
  padding: 80px 20px;
  text-align: center;
}
.apple-form {
  max-width: 420px;
  margin: 40px auto;
}
.input-group input,
.input-group textarea {
  width: 100%;
  background: #f5f5f7;
  border: none;
  padding: 14px 18px;
  border-radius: 14px;
  margin-bottom: 14px;
  font-size: 16px;
  outline: none;
}
.input-group input:focus,
.input-group textarea:focus {
  background: white;
  box-shadow: 0 0 0 2px #0071e3;
}
textarea {
  min-height: 110px;
}
button {
  background: black;
  color: white;
  border: none;
  padding: 14px;
  width: 100%;
  border-radius: 16px;
  font-size: 16px;
  cursor: pointer;
}
button.sending {
  opacity: 0.7;
  cursor: not-allowed;
}
.success,
.error {
  opacity: 0;
  transition: opacity 0.6s ease;
  margin-top: 15px;
}
.success.show,
.error.show {
  opacity: 1;
}

/* FOOTER */
footer {
  background: #e5e5e7;
  padding: 20px;
  text-align: center;
}

/* RESPONSIVE */
@media (max-width: 800px) {
  .values,
  .apple-cards,
  .plans {
    flex-direction: column;
    align-items: center;
  }
  .hero h1 {
    font-size: 36px;
  }
}
</style>
