<template>
  <div class="app">
    <!-- HEADER -->
    <header class="nav" role="navigation">
      <div class="brand">MJ Clean Pro Service</div>
      <nav class="nav-links">
        <a href="#accueil">Accueil</a>
        <a href="#services">Services</a>
        <a href="#tarifs">Tarifs</a>
        <a href="#contact" class="cta">Contact</a>
      </nav>
    </header>

    <main id="main-content">
      <!-- HERO -->
      <section id="accueil" class="hero" aria-labelledby="hero-title">
        <div class="hero-content">
          <h1 id="hero-title">
            La propreté.<br />
            <span>Version premium.</span>
          </h1>
          <p>
            MJ Clean Pro Service vous propose un service de nettoyage professionnel, fiable et
            adapté à vos besoins.
          </p>
          <a href="#contact" class="hero-cta">Demander un devis</a>
        </div>
      </section>

      <!-- VALEURS -->
      <section class="values" aria-label="Nos valeurs">
        <article class="value">
          <h3>Simple</h3>
          <p>Tarifs clairs et services transparents.</p>
        </article>
        <article class="value">
          <h3>Humain</h3>
          <p>Une entreprise familiale à l’écoute et proche de vous.</p>
        </article>
        <article class="value">
          <h3>Efficace</h3>
          <p>Un résultat professionnel à chaque passage.</p>
        </article>
      </section>

      <!-- SERVICES -->
      <section id="services" class="services" aria-labelledby="services-title">
        <h2 id="services-title" class="section-title">Nos services</h2>
        <div class="services-grid">
          <article class="service-card">
            <div class="icon" aria-hidden="true">🧹</div>
            <h3>Nettoyage ponctuel</h3>
            <p>Intervention rapide selon vos besoins.</p>
          </article>

          <article class="service-card highlight">
            <div class="icon" aria-hidden="true">📆</div>
            <h3>Contrat régulier</h3>
            <p>Un intérieur propre toute l’année, sans souci.</p>
          </article>

          <article class="service-card">
            <div class="icon" aria-hidden="true">🤝</div>
            <h3>Aide à domicile</h3>
            <p>Un accompagnement personnalisé au quotidien.</p>
          </article>
        </div>
      </section>

      <!-- TARIFS -->
      <section id="tarifs" class="pricing" aria-labelledby="pricing-title">
        <h2 id="pricing-title">Des tarifs horaires simples et transparents</h2>
        <p class="muted">Au plus proche de vos besoins</p>

        <div class="plans">
          <article class="plan">
            <h3>Occasionnel</h3>
            <p class="price">14,75 €</p>
            <p class="plan-desc">TTC après crédit d’impôt</p>
          </article>

          <article class="plan highlight">
            <h3>Abonnement</h3>
            <p class="price">20 €</p>
            <p class="plan-desc">TTC après crédit d’impôt</p>
          </article>

          <article class="plan">
            <h3>Aide à domicile</h3>
            <p class="price">22 €</p>
            <p class="plan-desc">TTC après crédit d’impôt</p>
          </article>
        </div>
      </section>

      <!-- CONTACT -->
      <section id="contact" class="contact" aria-labelledby="contact-title">
        <h2 id="contact-title">Contactez MJ Clean</h2>
        <p>Réponse rapide et devis gratuit</p>
        <a class="contact-mail" href="mailto:mjclean.proservices29@gmail.com">
          ✉ mjclean.proservices29@gmail.com
        </a>
      </section>
    </main>

    <footer>© {{ new Date().getFullYear() }} MJ Clean Pro Service</footer>
  </div>
</template>

<style scoped>
/* VARIABLES */
.app {
  --bg-main: #faf6ef;
  --bg-soft: #f4ede4;
  --blue-dark: #203f70;
  --blue-accent: #4f7cff;
  --text-main: #1d1d1f;
  --text-muted: #6b7280;

  font-family: -apple-system, BlinkMacSystemFont, system-ui, sans-serif;
  background: var(--bg-main);
  color: var(--text-main);
}

/* HEADER */
.nav {
  position: sticky;
  top: 0;
  z-index: 10;
  background: rgba(255, 255, 255, 0.8);
  backdrop-filter: blur(12px);
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 16px 40px;
}

.nav-links a {
  margin-left: 20px;
  text-decoration: none;
  color: var(--blue-dark);
  font-weight: 500;
}

.nav-links a:hover {
  color: var(--blue-accent);
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
  background:
    url('assets/hero-cleaning.png') no-repeat right center / contain,
    linear-gradient(120deg, #faf6ef 0%, #f4ede4 60%);
}

.hero-content {
  max-width: 520px;
}

.hero h1 {
  font-size: 3.2rem;
  line-height: 1.1;
  color: var(--blue-dark);
}

.hero h1 span {
  color: var(--blue-accent);
}

.hero p {
  font-size: 1.1rem;
  margin: 24px 0 32px;
  color: var(--text-muted);
}

.hero-cta {
  background: var(--blue-dark);
  color: #fff;
  padding: 14px 28px;
  border-radius: 999px;
  text-decoration: none;
}

.hero-cta:hover {
  background: var(--blue-accent);
}

/* VALUES */
.values {
  display: flex;
  justify-content: center;
  gap: 60px;
  padding: 80px 20px;
  text-align: center;
}

/* SERVICES */
.services {
  padding: 80px 20px;
}

.section-title {
  text-align: center;
  margin-bottom: 48px;
}

.services-grid {
  display: flex;
  justify-content: center;
  gap: 30px;
}

.service-card {
  background: #fff;
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
  color: #fff;
}

/* PRICING */
.pricing {
  background: #fff;
  padding: 100px 20px;
  text-align: center;
}

.muted {
  color: var(--text-muted);
}

.plans {
  display: flex;
  justify-content: center;
  gap: 30px;
  margin-top: 40px;
}

.plan {
  background: var(--bg-soft);
  padding: 30px;
  border-radius: 24px;
  width: 200px;
}

.plan.highlight {
  background: var(--blue-dark);
  color: #fff;
}

.price {
  font-size: 2.6rem;
  font-weight: 700;
}

/* CONTACT */
.contact {
  padding: 80px 20px;
  text-align: center;
}

.contact-mail {
  color: var(--blue-dark);
  text-decoration: none;
  font-weight: 500;
}

/* FOOTER */
footer {
  background: #e9e4db;
  padding: 20px;
  text-align: center;
  font-size: 0.9rem;
}

/* RESPONSIVE */
@media (max-width: 900px) {
  .hero {
    background-position: center bottom;
    background-size: 80%;
    padding: 60px 20px;
  }

  .values,
  .services-grid,
  .plans {
    flex-direction: column;
    align-items: center;
  }

  .hero h1 {
    font-size: 2.2rem;
  }
}
</style>
