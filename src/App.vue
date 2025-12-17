<template>
  <div class="app">
    <!-- HEADER -->
    <header class="nav" role="navigation">
      <div class="brand">MJ Clean Pro Service</div>
      <nav class="nav-links">
        <a href="#accueil" class="optional">Accueil</a>
        <a href="#services" class="optional">Services</a>
        <a href="#tarifs" class="optional">Tarifs</a>
        <a href="#contact" class="cta">Contact</a>
      </nav>
    </header>

    <main id="main-content">
      <!-- HERO -->
      <section id="accueil" class="hero" aria-labelledby="hero-title">
        <div class="hero-content">
          <h1 id="hero-title">
            La propreté<br />
            <span>Version premium</span>
          </h1>
          <p>
            MJ Clean Pro Service vous propose un service de nettoyage professionnel, fiable et
            adapté à vos besoins
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
            <div class="icon taille-icone" aria-hidden="true">🧹</div>
            <h3>Nettoyage ponctuel</h3>
            <p>Intervention rapide selon vos besoins.</p>
          </article>

          <article class="service-card highlight">
            <div class="icon taille-icone" aria-hidden="true">📆</div>
            <h3>Contrat régulier</h3>
            <p>Un intérieur propre toute l’année, sans souci.</p>
          </article>

          <article class="service-card">
            <div class="icon taille-icone" aria-hidden="true">🤝</div>
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
            <p class="price">14,75 € *</p>
            <p class="plan-desc">* Tarif horaires TTC après crédit d’impôt</p>
            <p class="plan-desc">soit 29,50 € TTC</p>
          </article>

          <article class="plan highlight">
            <h3>2h—3h/semaine</h3>
            <p class="price">13,25 € *</p>
            <p class="plan-desc">* Tarif horaires TTC après crédit d’impôt</p>
            <p class="plan-desc">soit 26,50 € TTC</p>
          </article>

          <article class="plan">
            <h3>4h—5h/semaine</h3>
            <p class="price">13,10 € *</p>
            <p class="plan-desc">* Tarif horaires TTC après crédit d’impôt</p>
            <p class="plan-desc">soit 26,20 € TTC</p>
          </article>

          <article class="plan">
            <h3>6h—12h/semaine</h3>
            <p class="price">12,75 € *</p>
            <p class="plan-desc">* Tarif horaires TTC après crédit d’impôt</p>
            <p class="plan-desc">soit 25,50 € TTC</p>
          </article>

          <article class="plan">
            <h3>>12h/semaine</h3>
            <p class="price">12,60 € *</p>
            <p class="plan-desc">* Tarif horaires TTC après crédit d’impôt</p>
            <p class="plan-desc">soit 25,20 € TTC</p>
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

        <a class="contact-phone" href="tel:+33612345678"> 📞 06 12 34 56 78 </a>
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

.taille-icone {
  font-size: 3.1rem;
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
.optional {
  display: none;
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

  background:
    url('assets/hero-cleaning.png') no-repeat right center / cover,
    linear-gradient(120deg, #faf6ef 0%, #f4ede4 60%);

  background-position: 60%;
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

/* VALEURS – GRID */
.values {
  display: flex;
  flex-direction: column; /* ⬅️ empile sur téléphone */
  gap: 32px;
  padding: 80px 20px;
  max-width: 1000px;
  margin: auto;
  text-align: center;
}

/* SERVICES – GRID AUTO */
.services {
  padding: 80px 20px;
  text-align: center;
}

.services-grid {
  display: grid;
  gap: 32px;
  max-width: 1000px;
  margin: 40px auto 0;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
}

.service-card {
  background: #fff;
  padding: 40px 30px;
  border-radius: 28px;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.08);
}

.service-card.highlight {
  background: var(--blue-dark);
  color: #fff;
}

/* PRICING – GRID */
.pricing {
  background: #fff;
  padding: 100px 20px;
  text-align: center;
}

.plans {
  display: flex;
  flex-direction: column;
  gap: 32px;
  max-width: 900px;
  margin: 40px auto 0;
  grid-template-columns: repeat(6, minmax(0, 320px));
  justify-content: center;
}

.plan {
  background: var(--bg-soft);
  padding: 32px;
  border-radius: 24px;
}

.plan.highlight {
  background: var(--blue-dark);
  color: #fff;
}

.price {
  font-size: 2.4rem;
  font-weight: 700;
}

/* CONTACT */
.contact {
  padding: 80px 20px;
  text-align: center;
}
.contact-mail,
.contact-phone {
  display: block;
  margin-top: 12px;
  font-size: 1.1rem;
  color: var(--blue-dark);
  text-decoration: none;
  font-weight: 500;
}

.contact-mail:hover,
.contact-phone:hover {
  color: var(--blue-accent);
}

/* FOOTER */
footer {
  padding: 20px;
  text-align: center;
  background: #e9e4db;
}

/* TABLET+ */
@media (min-width: 768px) {
  .nav-links {
    display: block;
  }

  .hero {
    text-align: left;
    padding: 120px 8%;
  }

  .hero h1 {
    font-size: 3rem;
  }
}

/* Desktop */
@media (min-width: 1024px) {
  .hero {
    min-height: 90vh;
    padding: 0 8%;
    background-position: right center;
    background-size: contain;
    background:
      url('assets/hero-cleaning.png') no-repeat right center / contain,
      linear-gradient(120deg, #faf6ef 0%, #f4ede4 60%);
  }
  .optional {
    display: inline;
  }

  .hero h1 {
    font-size: 3.2rem;
  }

  .values {
    flex-direction: row;
  }

  .services-grid,
  .plans {
    flex-direction: row;
  }
  .values {
    flex-direction: row; /* ⬅️ côte à côte sur écran large */
  }

  .plans {
    display: grid;
    gap: 32px;
    max-width: 900px;
    margin: 40px auto 0;
    grid-template-columns: repeat(3, minmax(0, 320px));
    justify-content: center;
  }
}
</style>
