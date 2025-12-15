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
        <div class="hero-content">
          <h1>
            La propreté.<br />
            <span>Version premium.</span>
          </h1>

          <p>
            MJ Clean Pro Service vous offre un service de nettoyage complet, adapté à vos besoins
            spécifiques.
          </p>

          <a href="#contact" class="hero-cta">Demander un devis</a>
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
      <section id="services" class="services">
        <div class="service-card">
          <div class="icon">🧹</div>
          <h3>Nettoyage ponctuel</h3>
          <p>Intervention à la demande, rapide et efficace.</p>
        </div>

        <div class="service-card highlight">
          <div class="icon">📆</div>
          <h3>Contrat régulier</h3>
          <p>Sérénité et propreté durable toute l’année.</p>
        </div>

        <div class="service-card">
          <div class="icon">🤝</div>
          <h3>Aide à domicile</h3>
          <p>Assistance quotidienne adaptée à vos besoins.</p>
        </div>
      </section>

      <!-- TARIFS -->
      <section id="tarifs" class="pricing">
        <h2>Des tarifs simples et transparents.</h2>
        <p class="muted">Au plus proche de vos besoins</p>

        <div class="plans">
          <div class="plan">
            <h3>Occasionnel</h3>
            <p class="price">14.75€</p>
            <p>TTC après crédit d’impôt</p>
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
        <h2>Contactez MJ Clean</h2>
        <p>Réponse rapide, devis gratuit.</p>
        <p>✉ mjclean.proservices29@gmail.com</p>
      </section>
    </main>

    <footer>© MJ Clean Pro Service</footer>
  </div>
</template>

<style scoped>
/* PALETTE */
:root {
  --bg-main: #faf6ef;
  --bg-soft: #f4ede4;
  --blue-dark: #243a5e;
  --blue-accent: #4f7cff;
  --text-main: #1d1d1f;
  --text-muted: #6b7280;
}

/* GLOBAL */
.apple {
  font-family: -apple-system, BlinkMacSystemFont, system-ui;
  background: var(--bg-main);
  color: var(--text-main);
}

/* HEADER */
.nav {
  position: sticky;
  top: 0;
  z-index: 10;
  background: rgba(255, 255, 255, 0.75);
  backdrop-filter: blur(12px);
  display: flex;
  justify-content: space-between;
  padding: 18px 40px;
}

.nav a {
  margin-left: 20px;
  text-decoration: none;
  color: var(--blue-dark);
}

.cta {
  border: 1px solid var(--blue-dark);
  padding: 6px 14px;
  border-radius: 999px;
}

/* HERO */
.hero {
  min-height: 90vh;
  display: flex;
  align-items: center;
  padding: 0 8%;
  background: url('assets/hero-cleaning.png'), linear-gradient(120deg, #faf6ef 0%, #f4ede4 60%);
  background-repeat: no-repeat;
  background-position: right center;
  background-size: contain;
}

.hero-content {
  max-width: 520px;
}

.hero h1 {
  font-size: 54px;
  line-height: 1.1;
  color: var(--blue-dark);
}

.hero span {
  color: var(--blue-accent);
}

.hero p {
  font-size: 18px;
  margin: 24px 0 32px;
  color: var(--text-muted);
}

.hero-cta {
  background: var(--blue-dark);
  color: white;
  padding: 14px 28px;
  border-radius: 999px;
  text-decoration: none;
}

/* VALUES */
.values {
  display: flex;
  justify-content: center;
  gap: 60px;
  padding: 80px 20px;
}

/* SERVICES */
.services {
  display: flex;
  justify-content: center;
  gap: 30px;
  padding: 80px 20px;
}

.service-card {
  background: white;
  width: 260px;
  padding: 40px 30px;
  border-radius: 28px;
  text-align: center;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.08);
}

.service-card .icon {
  font-size: 42px;
  margin-bottom: 20px;
}

.service-card.highlight {
  background: var(--blue-dark);
  color: white;
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
  background: var(--bg-soft);
  padding: 30px;
  border-radius: 24px;
  width: 200px;
}

.plan.highlight {
  background: var(--blue-dark);
  color: white;
}

.price {
  font-size: 44px;
  font-weight: bold;
}

/* CONTACT */
.contact {
  padding: 80px 20px;
  text-align: center;
}

/* FOOTER */
footer {
  background: #e9e4db;
  padding: 20px;
  text-align: center;
}

/* RESPONSIVE */
@media (max-width: 900px) {
  .hero {
    background-position: center bottom;
    background-size: 80%;
    padding: 60px 20px;
  }

  .values,
  .services,
  .plans {
    flex-direction: column;
    align-items: center;
  }

  .hero h1 {
    font-size: 38px;
  }
}
</style>
