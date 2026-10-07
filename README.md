<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0, viewport-fit=cover">
  <title>TouteSolution — Prestations logistiques & assistance aux professionnels</title>
  <meta name="description" content="TouteSolution : Courses et achats pour entreprises, assistance logistique, aide aux hôtels et événements, montage/démontage, manutention, installation et rangement. Paris & IDF 24/7.">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,300..800;1,9..40,300..800&family=Fraunces:ital,opsz,wght@0,9..144,300..800;1,9..144,300..800&display=swap" rel="stylesheet">

  <style>
    :root {
      --bg-base: #FAF8F5;
      --bg-surface: #FFFFFF;
      --bg-subtle: #F0EAE1;
      --border-subtle: #DFD7CA;
      --border-strong: #C8BEB0;
      --text-main: #181B1F;
      --text-body: #4A525D;
      --text-muted: #737D8C;
      --brand-gold: #B38A38;
      --brand-gold-hover: #8C6506;
      --brand-gold-subtle: rgba(179, 138, 56, 0.12);
      --font-display: 'Fraunces', serif;
      --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
    }

    * { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; }
    body {
      font-family: var(--font-sans);
      background-color: var(--bg-base);
      color: var(--text-main);
      line-height: 1.5;
      padding-bottom: 70px;
    }

    .container {
      width: 100%;
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 16px;
    }

    /* En-tête */
    .fixed-header-wrapper {
      position: sticky;
      top: 0;
      z-index: 1000;
      background: rgba(250, 248, 245, 0.95);
      backdrop-filter: blur(10px);
      border-bottom: 1px solid var(--border-subtle);
    }
    .top-announcement {
      background: var(--bg-subtle);
      border-bottom: 1px solid var(--border-subtle);
      font-size: 0.72rem;
      padding: 4px 16px;
      display: flex;
      justify-content: space-between;
      color: var(--text-body);
    }
    .header-content {
      height: 64px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    .brand-logo { text-decoration: none; display: flex; flex-direction: column; }
    .brand-name { font-family: var(--font-display); font-size: 1.35rem; font-weight: 700; color: var(--text-main); }
    .brand-name span { color: var(--brand-gold); }
    .brand-sub { font-size: 0.65rem; color: var(--text-muted); text-transform: uppercase; letter-spacing: 0.5px; }

    .nav-links { display: none; gap: 20px; }
    @media (min-width: 900px) { .nav-links { display: flex; } }
    .nav-link { text-decoration: none; color: var(--text-body); font-size: 0.85rem; font-weight: 500; }
    .nav-link:hover { color: var(--brand-gold); }

    /* BOUTONS IDENTIQUES DEVIS & CONTACT */
    .btn-devis, .btn-contact, .hero-btn-primary, .btn-action-gold {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      background: var(--brand-gold);
      color: #FFFFFF !important;
      font-weight: 600;
      text-decoration: none;
      border: none;
      cursor: pointer;
      border-radius: 10px;
      transition: background 0.2s ease, transform 0.1s ease;
      font-size: 0.85rem;
      padding: 0 18px;
      height: 44px;
    }
    .btn-devis:hover, .btn-contact:hover, .hero-btn-primary:hover, .btn-action-gold:hover {
      background: var(--brand-gold-hover);
    }

    /* Grille de Prestations */
    .section-wrap { padding: 48px 0; border-bottom: 1px solid var(--border-subtle); }
    .section-kicker { font-size: 0.75rem; font-weight: 700; color: var(--brand-gold); text-transform: uppercase; letter-spacing: 1px; margin-bottom: 4px; }
    .section-title { font-family: var(--font-display); font-size: 1.8rem; margin-bottom: 12px; }
    .section-desc { font-size: 0.88rem; color: var(--text-body); margin-bottom: 24px; max-width: 600px; }

    .services-grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 16px;
    }
    @media (min-width: 640px) { .services-grid { grid-template-columns: repeat(2, 1fr); } }
    @media (min-width: 1024px) { .services-grid { grid-template-columns: repeat(3, 1fr); } }

    .service-card {
      background: var(--bg-surface);
      border: 1px solid var(--border-subtle);
      border-radius: 16px;
      padding: 20px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      cursor: pointer;
      transition: all 0.2s ease;
    }
    .service-card:hover {
      border-color: var(--brand-gold);
      transform: translateY(-2px);
      box-shadow: 0 6px 16px rgba(0,0,0,0.04);
    }
    .service-icon { font-size: 1.5rem; margin-bottom: 12px; }
    .service-title { font-family: var(--font-display); font-size: 1.05rem; font-weight: 600; margin-bottom: 6px; }
    .service-desc { font-size: 0.8rem; color: var(--text-body); line-height: 1.4; }
    .service-link { font-size: 0.75rem; font-weight: 700; color: var(--brand-gold); margin-top: 14px; display: inline-block; }

    /* Formulaire & Simulateur */
    .calc-card {
      background: var(--bg-surface);
      border: 1px solid var(--border-subtle);
      border-radius: 18px;
      padding: 24px;
    }
    .form-grid-2 { display: grid; grid-template-columns: 1fr; gap: 14px; margin-bottom: 14px; }
    @media (min-width: 640px) { .form-grid-2 { grid-template-columns: 1fr 1fr; } }

    .form-label { display: block; font-size: 0.75rem; font-weight: 700; color: var(--text-body); margin-bottom: 4px; text-transform: uppercase; }
    .select-input, .input-field, .textarea-field {
      width: 100%;
      height: 44px;
      padding: 0 12px;
      border: 1px solid var(--border-subtle);
      border-radius: 8px;
      font-size: 0.85rem;
      background: #FFFFFF;
      outline: none;
      font-family: inherit;
    }
    .textarea-field { height: 80px; padding: 10px; resize: vertical; }
    .select-input:focus, .input-field:focus, .textarea-field:focus { border-color: var(--brand-gold); }

    .custom-service-box { display: none; margin-top: 10px; }
    .custom-service-box.show { display: block; }

    /* Barre tactile mobile inférieure */
    .mobile-bottom-bar {
      position: fixed;
      bottom: 0;
      left: 0;
      right: 0;
      height: 60px;
      background: rgba(250, 248, 245, 0.98);
      border-top: 1px solid var(--border-subtle);
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      align-items: center;
      z-index: 999;
    }
    @media (min-width: 768px) { .mobile-bottom-bar { display: none; } }
    .mob-tab {
      display: flex;
      flex-direction: column;
      align-items: center;
      text-decoration: none;
      color: var(--text-muted);
      font-size: 0.65rem;
      font-weight: 600;
    }
  </style>
</head>
<body>

  <!-- HEADER -->
  <div class="fixed-header-wrapper">
    <div class="top-announcement">
      <div><strong>TouteSolution</strong> — Prestations logistiques & assistance aux professionnels</div>
      <div>24h/24 & 7j/7</div>
    </div>
    <div class="container header-content">
      <a href="#" class="brand-logo">
        <div class="brand-name">Toute<span>Solution</span></div>
        <span class="brand-sub">Prestations logistiques & assistance aux professionnels</span>
      </a>
      <nav class="nav-links">
        <a href="#services" class="nav-link">Prestations</a>
        <a href="#devis" class="nav-link">Devis</a>
        <a href="#contact" class="nav-link">Contact</a>
      </nav>
      <a href="tel:0774800964" class="btn-action-gold">📞 07 74 80 09 64</a>
    </div>
  </div>

  <!-- SECTION PRESTATIONS (Sans numéros, descriptions concises) -->
  <section class="section-wrap" id="services">
    <div class="container">
      <div class="section-kicker">Prestations</div>
      <h2 class="section-title">Prestations logistiques & assistance aux professionnels</h2>
      <p class="section-desc">Solutions opérationnelles et réactives pour entreprises, conciergeries et événements :</p>

      <div class="services-grid">
        <div class="service-card" onclick="selectServiceInForm('Courses et achats pour entreprises')">
          <div>
            <div class="service-icon">🛍️</div>
            <h3 class="service-title">Courses et achats pour entreprises</h3>
            <p class="service-desc">Approvisionnements urgents, achats professionnels et récupération express de commandes.</p>
          </div>
          <span class="service-link">Demander cette prestation &rarr;</span>
        </div>

        <div class="service-card" onclick="selectServiceInForm('Assistance logistique')">
          <div>
            <div class="service-icon">🚚</div>
            <h3 class="service-title">Assistance logistique</h3>
            <p class="service-desc">Renfort opérationnel sur site, régulation de flux et coordination logistique 24/7.</p>
          </div>
          <span class="service-link">Demander cette prestation &rarr;</span>
        </div>

        <div class="service-card" onclick="selectServiceInForm('Aide aux hôtels et événements')">
          <div>
            <div class="service-icon">🏨</div>
            <h3 class="service-title">Aide aux hôtels et événements</h3>
            <p class="service-desc">Appui logistique pour établissements hôteliers, salons, réceptions et événements.</p>
          </div>
          <span class="service-link">Demander cette prestation &rarr;</span>
        </div>

        <div class="service-card" onclick="selectServiceInForm('Montage / démontage')">
          <div>
            <div class="service-icon">🔧</div>
            <h3 class="service-title">Montage / démontage</h3>
            <p class="service-desc">Assemblage et démontage de mobilier professionnel, cloisons, stands et structures.</p>
          </div>
          <span class="service-link">Demander cette prestation &rarr;</span>
        </div>

        <div class="service-card" onclick="selectServiceInForm('Manutention')">
          <div>
            <div class="service-icon">📦</div>
            <h3 class="service-title">Manutention</h3>
            <p class="service-desc">Portage et déplacement de charges avec matériel pro (diables, chariots, sangles).</p>
          </div>
          <span class="service-link">Demander cette prestation &rarr;</span>
        </div>

        <div class="service-card" onclick="selectServiceInForm('Installation et rangement')">
          <div>
            <div class="service-icon">📐</div>
            <h3 class="service-title">Installation et rangement</h3>
            <p class="service-desc">Mise en place d’espaces de travail, agencement de salles et rangement soigné.</p>
          </div>
          <span class="service-link">Demander cette prestation &rarr;</span>
        </div>

        <div class="service-card" onclick="selectServiceInForm('Autre')">
          <div>
            <div class="service-icon">✨</div>
            <h3 class="service-title">Autre prestation sur-mesure</h3>
            <p class="service-desc">Un besoin spécifique ? Précisez votre demande pour un accompagnement dédié.</p>
          </div>
          <span class="service-link">Demander un devis &rarr;</span>
        </div>
      </div>
    </div>
  </section>

  <!-- SECTION DEVIS RAPIDE (Avec option Autre + Contact même couleur) -->
  <section class="section-wrap" id="devis">
    <div class="container">
      <div style="text-align: center; margin-bottom: 24px;">
        <div class="section-kicker">Devis & Réservation</div>
        <h2 class="section-title">Demandez votre devis d'intervention</h2>
        <p class="section-desc" style="margin: 0 auto;">Confirmation sous 15 minutes par notre équipe de régulation.</p>
      </div>

      <div class="calc-card" style="max-width: 760px; margin: 0 auto;">
        <form action="https://formsubmit.co/Toutesolution.75@gmail.com" method="POST">
          <input type="hidden" name="_subject" value="Demande d'intervention TouteSolution">
          
          <div style="margin-bottom: 14px;">
            <label class="form-label">Prestation souhaitée *</label>
            <select name="Prestation" id="form-service" class="select-input" onchange="checkFormService(this.value)">
              <option value="Courses et achats pour entreprises">Courses et achats pour entreprises</option>
              <option value="Assistance logistique">Assistance logistique</option>
              <option value="Aide aux hôtels et événements">Aide aux hôtels et événements</option>
              <option value="Montage / démontage">Montage / démontage</option>
              <option value="Manutention">Manutention</option>
              <option value="Installation et rangement">Installation et rangement</option>
              <option value="Autre">Autre (sur-mesure)</option>
            </select>

            <div class="custom-service-box" id="form-custom-box">
              <label class="form-label" style="color: var(--brand-gold); margin-top: 8px;">Précisez votre prestation *</label>
              <input type="text" name="PrecisionAutre" id="form-custom-input" class="input-field" placeholder="Détaillez votre besoin particulier...">
            </div>
          </div>

          <div class="form-grid-2">
            <div>
              <label class="form-label">Nom & Prénom *</label>
              <input type="text" name="Nom" required class="input-field" placeholder="Alexandre Mercier">
            </div>
            <div>
              <label class="form-label">Société / Établissement (optionnel)</label>
              <input type="text" name="Societe" class="input-field" placeholder="Société ou Établissement">
            </div>
          </div>

          <div class="form-grid-2">
            <div>
              <label class="form-label">Téléphone *</label>
              <input type="tel" name="Telephone" required class="input-field" placeholder="06 .. .. .. ..">
            </div>
            <div>
              <label class="form-label">E-mail *</label>
              <input type="email" name="Email" required class="input-field" placeholder="contact@entreprise.fr">
            </div>
          </div>

          <div style="margin-bottom: 18px;">
            <label class="form-label">Précisions sur la mission (optionnel)</label>
            <textarea name="Details" class="textarea-field" placeholder="Volume, contraintes d'accès ou horaires..."></textarea>
          </div>

          <!-- Boutons Devis et Contact : MÊME COULEUR -->
          <div style="display: flex; flex-direction: column; gap: 10px;">
            <button type="submit" class="btn-devis" style="width: 100%;">
              Envoyer ma demande de devis
            </button>
            <a href="tel:0774800964" class="btn-contact" style="width: 100%;">
              📞 Contacter directement : 07 74 80 09 64
            </a>
          </div>
        </form>
      </div>
    </div>
  </section>

  <!-- SECTION CONTACT (Même couleur) -->
  <section class="section-wrap" id="contact" style="background: var(--bg-subtle);">
    <div class="container" style="text-align: center;">
      <div class="section-kicker">Contact Direct</div>
      <h2 class="section-title">Permanence 24h/24 & 7j/7</h2>
      <div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 12px; margin-top: 16px;">
        <a href="tel:0774800964" class="btn-contact">📞 07 74 80 09 64</a>
        <a href="mailto:Toutesolution.75@gmail.com" class="btn-contact">✉️ Toutesolution.75@gmail.com</a>
      </div>
    </div>
  </section>

  <!-- NAVIGATION MOBILE FIXE -->
  <nav class="mobile-bottom-bar">
    <a href="#" class="mob-tab"><span>🏠</span><span>Accueil</span></a>
    <a href="#services" class="mob-tab"><span>💼</span><span>Prestations</span></a>
    <a href="#devis" class="mob-tab"><span>📝</span><span>Devis</span></a>
    <a href="tel:0774800964" class="mob-tab" style="color: var(--brand-gold);"><span>📞</span><span>Appel</span></a>
  </nav>

  <script>
    function selectServiceInForm(serviceName) {
      const sel = document.getElementById('form-service');
      if (sel) {
        sel.value = serviceName;
        checkFormService(serviceName);
      }
      const devisEl = document.getElementById('devis');
      if (devisEl) devisEl.scrollIntoView({ behavior: 'smooth' });
    }

    function checkFormService(val) {
      const box = document.getElementById('form-custom-box');
      const input = document.getElementById('form-custom-input');
      if (val === 'Autre') {
        box.classList.add('show');
        if (input) input.required = true;
      } else {
        box.classList.remove('show');
        if (input) input.required = false;
      }
    }
  </script>
</body>
</html>
