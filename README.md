<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
<meta name="theme-color" content="#0D1217">
<title>Toute Solution — Transport & Logistique à Paris</title>
<meta name="description" content="Toute Solution — transport, livraison et logistique à Paris et en Île-de-France. Demande de devis et contact rapide.">
<meta property="og:title" content="TouteSolution — Coursier Express Paris 24h/24">
<meta property="og:description" content="Livraison express et déménagement à Paris et en Île-de-France. Disponible 24h/24, 7j/7. Devis gratuit et rapide.">
<meta property="og:type" content="website">
<link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 64 64'%3E%3Crect width='64' height='64' fill='%23191919'/%3E%3Ctext x='32' y='44' font-family='Georgia,serif' font-size='34' font-weight='700' fill='%23D4A843' text-anchor='middle'%3ET%3C/text%3E%3C/svg%3E">

<!-- Fonts -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600;700&family=Fraunces:ital,wght@0,300;0,600;0,700;1,300;1,600&display=swap" rel="stylesheet">

<style>
/* ==========================================
   1. VARIABLES & RESET STYLES
   ========================================== */
*, *::before, *::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

:root {
  /* Brand Palette */
  --brand-gold: #D4A843;
  --brand-gold-light: #F0C96A;
  --brand-gold-dark: #96721C;
  
  /* Neutral Dark Tones */
  --bg-dark: #191919;
  --bg-card: #242424;
  --bg-input: #2E2E2E;
  
  /* Borders & Dividers */
  --border-charcoal: #3A3A3A;
  --border-light: #4A4A47;

  /* Typography Colors */
  --text-muted: #B7B1A3;
  --text-placeholder: #9A9488;
  --text-faint: #726C60;
  --text-cream: #F0EBE0;
  --text-warm-white: #E8E2D4;
}

html {
  scroll-behavior: smooth;
  scroll-padding-top: 64px;
}

body {
  font-family: 'DM Sans', sans-serif;
  background: var(--bg-dark);
  color: var(--text-cream);
  overflow-x: hidden;
  font-size: 16px;
  -webkit-font-smoothing: antialiased;
}

/* Custom minimal scrollbar */
::-webkit-scrollbar {
  width: 4px;
}
::-webkit-scrollbar-track {
  background: var(--bg-dark);
}
::-webkit-scrollbar-thumb {
  background: var(--brand-gold-dark);
}

a {
  color: inherit;
  text-decoration: none;
}

/* ==========================================
   2. TOPBAR & SYSTEM STATUS
   ========================================== */
.topbar {
  background: var(--bg-card);
  border-bottom: 1px solid var(--border-charcoal);
  padding: 9px 6%;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.topbar-left {
  font-size: .7rem;
  color: var(--text-placeholder);
  letter-spacing: .3px;
}

.topbar-right {
  display: flex;
  align-items: center;
  gap: 28px;
}

.topbar-right a {
  font-size: .7rem;
  color: var(--text-placeholder);
  transition: color .2s ease;
}

.topbar-right a:hover {
  color: var(--brand-gold);
}

.live-status {
  display: flex;
  align-items: center;
  gap: 6px;
  font-size: .7rem;
  color: var(--text-placeholder);
}

.live-dot {
  width: 6px;
  height: 6px;
  border-radius: 50%;
  background: #4ade80;
  flex-shrink: 0;
  box-shadow: 0 0 6px rgba(74, 222, 128, 0.6);
  animation: pulse 2.4s ease-in-out infinite;
}

@keyframes pulse {
  0%, 100% { opacity: 1; transform: scale(1); }
  50% { opacity: .4; transform: scale(.8); }
}

/* ==========================================
   3. HEADER & NAVIGATION
   ========================================== */
nav {
  background: var(--bg-dark);
  border-bottom: 1px solid var(--border-charcoal);
  height: 64px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 6%;
  position: sticky;
  top: 0;
  z-index: 300;
}

.nav-logo {
  font-family: 'Fraunces', serif;
  font-size: 1.25rem;
  font-weight: 600;
  letter-spacing: -.5px;
  color: var(--text-cream);
}

.nav-logo b {
  color: var(--brand-gold);
  font-weight: 600;
}

.nav-links {
  display: flex;
  list-style: none;
  gap: 0;
}

.nav-links a {
  font-size: .72rem;
  font-weight: 500;
  color: var(--text-placeholder);
  padding: 0 18px;
  height: 64px;
  display: flex;
  align-items: center;
  letter-spacing: .5px;
  text-transform: uppercase;
  transition: color .2s, border-color .2s;
  border-bottom: 2px solid transparent;
  margin-bottom: -1px;
}

.nav-links a:hover {
  color: var(--text-cream);
  border-bottom-color: var(--brand-gold);
}

.nav-actions {
  display: flex;
  align-items: center;
  gap: 14px;
}

.nav-tel {
  font-size: .8rem;
  font-weight: 600;
  color: var(--brand-gold);
}

.nav-cta {
  background: var(--brand-gold);
  color: var(--bg-dark);
  padding: 9px 22px;
  font-size: .7rem;
  font-weight: 700;
  letter-spacing: .8px;
  text-transform: uppercase;
  transition: background .2s ease;
}

.nav-cta:hover {
  background: var(--brand-gold-light);
}

.nav-hamburger {
  display: none;
  flex-direction: column;
  justify-content: center;
  gap: 5px;
  width: 32px;
  height: 32px;
  background: none;
  border: none;
  cursor: pointer;
  padding: 0;
}

.nav-hamburger span {
  display: block;
  width: 100%;
  height: 1.5px;
  background: var(--text-cream);
  transition: transform .25s ease, opacity .25s ease;
}

.nav-hamburger.open span:nth-child(1) {
  transform: translateY(6.5px) rotate(45deg);
}

.nav-hamburger.open span:nth-child(2) {
  opacity: 0;
}

.nav-hamburger.open span:nth-child(3) {
  transform: translateY(-6.5px) rotate(-45deg);
}

.mobile-menu {
  display: none;
  position: fixed;
  top: 58px;
  left: 0;
  right: 0;
  bottom: 0;
  background: var(--bg-dark);
  z-index: 250;
  padding: 8px 6% 32px;
  overflow-y: auto;
  transform: translateY(-12px);
  opacity: 0;
  pointer-events: none;
  transition: transform .25s ease, opacity .25s ease;
}

.mobile-menu.open {
  display: block;
  transform: translateY(0);
  opacity: 1;
  pointer-events: auto;
}

.mobile-menu ul {
  list-style: none;
}

.mobile-menu a {
  display: block;
  padding: 16px 0;
  border-bottom: 1px solid var(--border-charcoal);
  font-family: 'Fraunces', serif;
  font-size: 1.2rem;
  color: var(--text-cream);
}

.mobile-menu-contact {
  margin-top: 20px;
  padding-top: 20px;
  display: flex;
  flex-direction: column;
  gap: 14px;
}

.mobile-menu-contact a {
  color: var(--brand-gold);
  font-weight: 700;
  font-size: 1rem;
}

.mobile-menu-cta {
  display: block;
  margin-top: 20px;
  background: var(--brand-gold);
  color: var(--bg-dark);
  text-align: center;
  padding: 14px;
  font-family: 'DM Sans', sans-serif;
  font-size: .72rem;
  font-weight: 700;
  letter-spacing: 1.5px;
  text-transform: uppercase;
}

/* ==========================================
   4. HERO SECTION
   ========================================== */
.hero {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  padding: 0 6% 72px;
  position: relative;
  overflow: hidden;
  background: var(--bg-dark);
  border-bottom: 1px solid var(--border-charcoal);
}

.hero-bg-text {
  position: absolute;
  bottom: -60px;
  right: -40px;
  font-family: 'Fraunces', serif;
  font-size: 28vw;
  font-weight: 700;
  font-style: italic;
  color: transparent;
  -webkit-text-stroke: 1px rgba(212,168,67,.06);
  line-height: 1;
  pointer-events: none;
  user-select: none;
  white-space: nowrap;
}

.hero-line {
  position: absolute;
  top: 0;
  left: 6%;
  right: 6%;
  height: 1px;
  background: var(--border-charcoal);
}

.hero-content {
  position: relative;
  z-index: 1;
  max-width: 800px;
}

.hero-eyebrow {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-bottom: 32px;
}

.hero-eyebrow-line {
  width: 32px;
  height: 1px;
  background: var(--brand-gold);
}

.hero-eyebrow-txt {
  font-size: .68rem;
  font-weight: 600;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--brand-gold);
}

.hero h1 {
  font-family: 'Fraunces', serif;
  font-size: clamp(3.2rem, 7vw, 6.5rem);
  font-weight: 300;
  line-height: .95;
  letter-spacing: -3px;
  color: var(--text-cream);
  margin-bottom: 0;
}

.hero h1 em {
  font-style: italic;
  color: var(--brand-gold);
}

.hero h1 strong {
  font-weight: 700;
}

.hero-caption {
  font-size: .95rem;
  font-weight: 400;
  color: var(--text-muted);
  line-height: 1.75;
  max-width: 460px;
  margin-top: 28px;
}

.hero-actions {
  display: flex;
  gap: 12px;
  flex-wrap: wrap;
  margin-top: 36px;
}

.btn-primary {
  background: var(--brand-gold);
  color: var(--bg-dark);
  padding: 14px 36px;
  font-size: .72rem;
  font-weight: 700;
  letter-spacing: 1px;
  text-transform: uppercase;
  transition: background .2s ease;
}

.btn-primary:hover {
  background: var(--brand-gold-light);
}

.btn-secondary {
  background: transparent;
  color: var(--text-cream);
  padding: 14px 36px;
  font-size: .72rem;
  font-weight: 500;
  letter-spacing: 1px;
  text-transform: uppercase;
  border: 1px solid var(--border-light);
  transition: all .2s ease;
}

.btn-secondary:hover {
  border-color: var(--brand-gold);
  color: var(--brand-gold);
}

.hero-stats {
  display: flex;
  gap: 0;
  margin-top: 60px;
  padding-top: 32px;
  border-top: 1px solid var(--border-charcoal);
}

.stat-box {
  padding-right: 48px;
  border-right: 1px solid var(--border-charcoal);
}

.stat-box:not(:first-child) {
  padding-left: 48px;
}

.stat-box:last-child {
  border-right: none;
}

.stat-value {
  font-family: 'Fraunces', serif;
  font-size: 2rem;
  font-weight: 600;
  color: var(--brand-gold);
  line-height: 1;
  letter-spacing: -1px;
}

.stat-label {
  font-size: .6rem;
  font-weight: 500;
  color: var(--text-placeholder);
  text-transform: uppercase;
  letter-spacing: 2px;
  margin-top: 4px;
}

/* ==========================================
   5. SECTION STRUCTURING (GENERIC)
   ========================================== */
.section-wrapper {
  border-bottom: 1px solid var(--border-charcoal);
}

.section-header {
  padding: 56px 6% 36px;
  border-bottom: 1px solid var(--border-charcoal);
}

.section-eyebrow {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-bottom: 12px;
}

.section-eyebrow-line {
  width: 22px;
  height: 1px;
  background: var(--brand-gold);
}

.section-kicker {
  font-size: .62rem;
  font-weight: 600;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--brand-gold);
}

.section-title {
  font-family: 'Fraunces', serif;
  font-size: clamp(1.8rem, 3.5vw, 3rem);
  font-weight: 300;
  color: var(--text-cream);
  letter-spacing: -1px;
  line-height: 1.05;
}

.section-title em {
  font-style: italic;
}

.section-desc {
  font-size: .88rem;
  font-weight: 400;
  color: var(--text-muted);
  margin-top: 8px;
  max-width: 520px;
  line-height: 1.8;
}

/* ==========================================
   6. SERVICES TABLE
   ========================================== */
.services-row {
  display: grid;
  grid-template-columns: 200px 1fr 120px;
  border-bottom: 1px solid var(--border-charcoal);
  transition: background .15s ease;
}

.services-row:hover {
  background: var(--bg-card);
}

.services-row:hover .service-num {
  color: var(--brand-gold);
}

.service-meta {
  padding: 24px 28px;
  border-right: 1px solid var(--border-charcoal);
}

.service-num {
  font-size: .62rem;
  font-weight: 600;
  letter-spacing: 2px;
  color: var(--text-faint);
  text-transform: uppercase;
  margin-bottom: 6px;
  transition: color .2s ease;
}

.service-name {
  font-size: .9rem;
  font-weight: 600;
  color: var(--text-cream);
  letter-spacing: -.2px;
}

.service-content {
  padding: 24px 32px;
  border-right: 1px solid var(--border-charcoal);
}

.service-desc {
  font-size: .8rem;
  font-weight: 400;
  color: var(--text-muted);
  line-height: 1.85;
}

.service-vehicle {
  padding: 24px 20px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.vehicle-badge {
  font-size: .58rem;
  font-weight: 700;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--brand-gold-dark);
  text-align: center;
  line-height: 1.7;
}

/* ==========================================
   7. VEHICLE FLEET CARDS
   ========================================== */
.fleet-section {
  background: var(--bg-card);
}

.fleet-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  border-left: 1px solid var(--border-charcoal);
  border-top: 1px solid var(--border-charcoal);
}

.vehicle-card {
  background: var(--bg-dark);
  border-right: 1px solid var(--border-charcoal);
  border-bottom: 1px solid var(--border-charcoal);
  padding: 28px 24px;
  position: relative;
  transition: background .15s ease;
}

.vehicle-card:hover {
  background: var(--bg-card);
}

.vehicle-card.premium {
  background: #1A1300;
  border-top: 2px solid var(--brand-gold);
}

.vehicle-card.premium:hover {
  background: #201700;
}

.vehicle-icon-wrap {
  width: 52px;
  height: 36px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: var(--bg-card);
  border: 1px solid var(--border-charcoal);
  color: var(--brand-gold);
  margin-bottom: 18px;
}

.vehicle-icon-wrap svg {
  width: 30px;
  height: 20px;
}

.vehicle-card.premium .vehicle-icon-wrap {
  background: #120E00;
  border-color: var(--brand-gold-dark);
  color: var(--brand-gold-light);
}

.vehicle-card:hover .vehicle-icon-wrap {
  border-color: var(--brand-gold);
}

.vehicle-index {
  font-size: .58rem;
  font-weight: 700;
  letter-spacing: 2.5px;
  color: var(--text-placeholder);
  text-transform: uppercase;
  margin-bottom: 12px;
  transition: color .2s ease;
}

.vehicle-card.premium .vehicle-index {
  color: var(--brand-gold-dark);
}

.vehicle-title {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  gap: 8px;
  font-family: 'Fraunces', serif;
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--text-cream);
  letter-spacing: -.3px;
  margin-bottom: 2px;
}

.reco-badge {
  font-family: 'DM Sans', sans-serif;
  font-size: .52rem;
  font-weight: 700;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  color: var(--bg-dark);
  background: var(--brand-gold);
  padding: 3px 7px;
}

.vehicle-sub {
  font-size: .72rem;
  font-weight: 400;
  color: var(--text-placeholder);
  margin-bottom: 14px;
}

.card-divider {
  height: 1px;
  background: var(--border-charcoal);
  margin-bottom: 14px;
}

.vehicle-features {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
}

.feature-item {
  font-size: .68rem;
  font-weight: 500;
  color: var(--text-muted);
  background: var(--bg-card);
  border: 1px solid var(--border-charcoal);
  padding: 5px 10px;
  line-height: 1.3;
}

.vehicle-card.premium .feature-item {
  background: #120E00;
  border-color: rgba(212, 168, 67, .25);
  color: var(--text-warm-white);
}

.vehicle-eta {
  margin-top: 16px;
  padding: 8px 12px;
  background: var(--bg-card);
  font-size: .62rem;
  font-weight: 300;
  color: var(--text-placeholder);
  line-height: 1.6;
}

.vehicle-card.premium .vehicle-eta {
  background: #120E00;
  color: var(--brand-gold-dark);
}

.vehicle-eta b {
  color: var(--brand-gold);
  font-weight: 600;
}

.status-tag {
  position: absolute;
  top: 14px;
  right: 14px;
  font-size: .54rem;
  font-weight: 700;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  color: #4ade80;
  background: rgba(74, 222, 128, .06);
  border: 1px solid rgba(74, 222, 128, .15);
  padding: 3px 7px;
}

.status-tag.on-demand {
  color: var(--brand-gold);
  background: rgba(212, 168, 67, .08);
  border-color: rgba(212, 168, 67, .3);
}

.status-tag.soon {
  color: var(--text-placeholder);
  background: rgba(255, 255, 255, .04);
  border-color: var(--border-light);
}


/* ==========================================
   8. INTERACTIVE COVERAGE MAP
   ========================================== */
.map-section {
  background: var(--bg-card);
}

.map-layout {
  display: grid;
  grid-template-columns: 1fr 320px;
}

.zone-map-visual {
  height: 500px;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
  background:
    radial-gradient(circle at center, rgba(212,168,67,.05) 0%, transparent 60%),
    var(--bg-dark);
}

.zone-map-visual::before {
  content: '';
  position: absolute;
  inset: 0;
  background-image:
    linear-gradient(var(--border-charcoal) 1px, transparent 1px),
    linear-gradient(90deg, var(--border-charcoal) 1px, transparent 1px);
  background-size: 48px 48px;
  opacity: .2;
}

.zone-map-svg {
  position: relative;
  z-index: 1;
  width: 100%;
  height: 100%;
}

.zone-map-svg .dept-region {
  stroke-width: 2;
  stroke-linejoin: round;
  transition: filter .2s ease;
  cursor: pointer;
}

.zone-map-svg .dept-region:hover {
  filter: brightness(1.2);
}

.zone-map-svg .zone-1-fill {
  fill: var(--brand-gold);
  stroke: var(--brand-gold-light);
}

.zone-map-svg .zone-2-fill {
  fill: #241B04;
  stroke: var(--brand-gold-dark);
}

.zone-map-svg .zone-3-fill {
  fill: var(--bg-card);
  stroke: var(--border-light);
}

.zone-map-svg .dept-label {
  font-family: 'DM Sans', sans-serif;
  font-weight: 700;
  text-anchor: middle;
  pointer-events: none;
}

.zone-map-svg .dept-label.zone-1 {
  fill: var(--bg-dark);
  font-size: 15px;
}

.zone-map-svg .dept-label.zone-2 {
  fill: var(--brand-gold-light);
  font-size: 13px;
}

.zone-map-svg .dept-label.zone-3 {
  fill: var(--text-cream);
  font-size: 14px;
}

.zone-map-svg .paris-callout-line {
  stroke: var(--brand-gold);
  stroke-width: 1;
}

.zone-map-svg .paris-callout-dot {
  fill: var(--brand-gold);
}

.zone-map-svg .paris-callout-text {
  font-family: 'Fraunces', serif;
  font-weight: 600;
  font-size: 15px;
  fill: var(--brand-gold);
}

.zone-map-legend-inline {
  position: absolute;
  top: 24px;
  right: 24px;
  z-index: 2;
  display: flex;
  flex-direction: column;
  gap: 6px;
  font-family: 'DM Sans', sans-serif;
  font-size: .62rem;
  color: var(--text-placeholder);
}

.zone-map-legend-inline span {
  display: flex;
  align-items: center;
  gap: 7px;
}

.zone-map-legend-inline i {
  width: 9px;
  height: 9px;
  display: inline-block;
  border-radius: 2px;
}

.zone-map-legend-inline .dot-1 { background: var(--brand-gold); }
.zone-map-legend-inline .dot-2 { background: var(--brand-gold-dark); }
.zone-map-legend-inline .dot-3 { background: var(--border-light); }

.zone-map-caption {
  position: absolute;
  left: 24px;
  bottom: 20px;
  z-index: 2;
  font-size: .62rem;
  letter-spacing: 1px;
  text-transform: uppercase;
  color: var(--text-placeholder);
}

.zone-map-caption b {
  color: var(--brand-gold);
}

.map-sidebar {
  padding: 28px 24px;
  display: flex;
  flex-direction: column;
  gap: 0;
  border-left: 1px solid var(--border-charcoal);
}

.sidebar-title {
  font-size: .58rem;
  font-weight: 700;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--brand-gold);
  margin-bottom: 18px;
}

.map-zone-row {
  display: flex;
  border: 1px solid var(--border-charcoal);
  margin-bottom: 1px;
}

.map-zone-row:last-of-type {
  margin-bottom: 0;
}

.zone-badge {
  font-size: .62rem;
  font-weight: 700;
  letter-spacing: 1px;
  padding: 16px 14px;
  min-width: 64px;
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
}

.zone-1 .zone-badge {
  background: rgba(212, 168, 67, .15);
  color: var(--brand-gold);
  border-right: 1px solid var(--border-charcoal);
}

.zone-2 .zone-badge {
  background: rgba(150, 114, 28, .1);
  color: var(--brand-gold-dark);
  border-right: 1px solid var(--border-charcoal);
}

.zone-3 .zone-badge {
  background: var(--bg-input);
  color: var(--text-placeholder);
  border-right: 1px solid var(--border-charcoal);
}

.zone-info {
  padding: 14px 16px;
}

.zone-name {
  font-size: .75rem;
  font-weight: 600;
  color: var(--text-cream);
  margin-bottom: 3px;
}

.zone-details {
  font-size: .7rem;
  font-weight: 400;
  color: var(--text-muted);
  line-height: 1.6;
}

.zone-quick-contact {
  margin-top: 16px;
  padding: 16px;
  background: var(--bg-dark);
  border: 1px solid var(--border-charcoal);
  border-left: 2px solid var(--brand-gold);
}

.quick-contact-text {
  font-size: .7rem;
  font-weight: 400;
  color: var(--text-muted);
  line-height: 1.6;
  margin-bottom: 10px;
}

.quick-contact-phone {
  font-size: .9rem;
  font-weight: 700;
  color: var(--brand-gold);
}

.sidebar-live-footer {
  display: flex;
  align-items: center;
  gap: 7px;
  margin-top: 16px;
  font-size: .65rem;
  color: var(--text-placeholder);
}

.zones-summary {
  display: flex;
  justify-content: center;
}

.zones-summary-left {
  padding: 48px 6%;
  width: 100%;
  max-width: 720px;
}

.quick-stats-table {
  margin-top: 20px;
  border: 1px solid var(--border-charcoal);
}

.stats-row {
  display: grid;
  grid-template-columns: 100px 1fr;
  border-bottom: 1px solid var(--border-charcoal);
}

.stats-row:last-child {
  border-bottom: none;
}

.stats-key {
  background: var(--bg-card);
  padding: 12px 14px;
  font-size: .6rem;
  font-weight: 700;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  color: var(--brand-gold);
  border-right: 1px solid var(--border-charcoal);
  display: flex;
  align-items: center;
}

.stats-val {
  padding: 12px 14px;
  font-size: .78rem;
  font-weight: 400;
  color: var(--text-muted);
  display: flex;
  align-items: center;
}

/* ==========================================
   9. FARE ESTIMATOR
   ========================================== */
.estimator-section {
  background: var(--bg-dark);
  padding: 64px 6%;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 80px;
  align-items: start;
  border-bottom: 1px solid var(--border-charcoal);
}

.estimator-label {
  font-size: .58rem;
  font-weight: 600;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--text-placeholder);
  display: block;
  margin-bottom: 7px;
  margin-top: 16px;
}

.estimator-label:first-child {
  margin-top: 0;
}

.estimator-select, .estimator-input {
  width: 100%;
  background: var(--bg-card);
  border: 1px solid var(--border-charcoal);
  color: var(--text-cream);
  padding: 11px 14px;
  font-family: 'DM Sans', sans-serif;
  font-size: .8rem;
  font-weight: 300;
  outline: none;
  transition: border-color .2s ease, background .2s ease;
  appearance: none;
}

.estimator-select {
  cursor: pointer;
  padding-right: 38px;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='12' height='7' viewBox='0 0 12 7'%3E%3Cpath fill='%23D4A843' d='M6 7L0 0h12z'/%3E%3C/svg%3E");
  background-repeat: no-repeat;
  background-position: right 14px center;
}

.estimator-select:hover {
  border-color: var(--text-placeholder);
  background-color: #262622;
}

.estimator-select:focus, .estimator-input:focus {
  border-color: var(--brand-gold);
}

.estimator-select option {
  background: var(--bg-card);
  color: var(--text-cream);
}

.select-options-hint {
  margin-top: 7px;
  font-size: .62rem;
  line-height: 1.45;
  color: var(--text-faint);
}

.estimator-select, .select-field {
  background-color: var(--bg-card);
}

.estimator-select:hover, .select-field:hover {
  border-color: var(--brand-gold);
}

.field-error {
  display: none;
  font-size: .66rem;
  color: #E8967A;
  margin-top: 6px;
  font-weight: 500;
}

.field-error.visible {
  display: block;
}

.estimator-select.field-invalid {
  border-color: #E8967A;
}

.estimator-row {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 10px;
}

.estimator-button {
  width: 100%;
  background: var(--brand-gold);
  color: var(--bg-dark);
  border: none;
  padding: 13px;
  font-family: 'DM Sans', sans-serif;
  font-size: .68rem;
  font-weight: 700;
  letter-spacing: 2px;
  text-transform: uppercase;
  cursor: pointer;
  transition: background .2s ease;
  margin-top: 16px;
}

.estimator-button:hover {
  background: var(--brand-gold-light);
}

.estimator-result {
  display: none; /* Managed by JS */
  margin-top: 14px;
  padding: 14px 16px;
  background: var(--bg-card);
  border-left: 2px solid var(--brand-gold);
}

.estimator-price {
  font-family: 'Fraunces', serif;
  font-size: 1.6rem;
  font-weight: 600;
  color: var(--brand-gold);
  letter-spacing: -1px;
}

.estimator-note {
  font-size: .68rem;
  font-weight: 400;
  color: var(--text-placeholder);
  margin-top: 4px;
  line-height: 1.6;
}

/* ==========================================
   10. QUOTE FORM & PROMISES
   ========================================== */
.quote-layout {
  display: grid;
  grid-template-columns: 300px 1fr;
}

.quote-sidebar {
  padding: 48px 36px;
  border-right: 1px solid var(--border-charcoal);
  background: var(--bg-card);
}

.quote-content {
  padding: 48px 6%;
}

.promise-list {
  margin-top: 20px;
  border: 1px solid var(--border-charcoal);
}

.promise-row {
  display: flex;
  border-bottom: 1px solid var(--border-charcoal);
}

.promise-row:last-child {
  border-bottom: none;
}

.promise-index {
  background: var(--brand-gold);
  color: var(--bg-dark);
  font-size: .65rem;
  font-weight: 700;
  padding: 14px 14px;
  min-width: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.promise-text {
  padding: 14px 14px;
  font-size: .78rem;
  font-weight: 400;
  color: var(--text-muted);
  line-height: 1.5;
}

.direct-contact-card {
  margin-top: 20px;
  background: var(--brand-gold);
  color: var(--bg-dark);
  padding: 24px;
}

.direct-label {
  font-size: .58rem;
  font-weight: 700;
  letter-spacing: 2.5px;
  text-transform: uppercase;
  opacity: .6;
  margin-bottom: 10px;
}

.direct-phone {
  font-family: 'Fraunces', serif;
  font-size: 1.4rem;
  font-weight: 600;
  letter-spacing: -.5px;
  margin-bottom: 4px;
}

.direct-email {
  font-size: .75rem;
  font-weight: 400;
  opacity: .75;
}

.direct-hours {
  font-size: .62rem;
  opacity: .55;
  margin-top: 8px;
  letter-spacing: .3px;
}

.form-wrapper {
  background: var(--bg-dark);
  border: 1px solid var(--border-charcoal);
}

.form-header {
  background: var(--brand-gold);
  color: var(--bg-dark);
  padding: 18px 24px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.form-header-title {
  font-size: .82rem;
  font-weight: 700;
  letter-spacing: -.2px;
}

.form-header-sub {
  font-size: .6rem;
  opacity: .6;
  letter-spacing: .3px;
}

.form-body {
  padding: 24px;
}

.form-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 12px;
}

.form-group {
  display: flex;
  flex-direction: column;
  gap: 6px;
  margin-bottom: 12px;
}

.form-group:last-child {
  margin-bottom: 0;
}

.form-grid .form-group:last-child {
  margin-bottom: 12px;
}

.form-label {
  font-size: .56rem;
  font-weight: 700;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--text-placeholder);
}

.input-field, .select-field, .textarea-field {
  width: 100%;
  background: var(--bg-card);
  border: 1px solid var(--border-charcoal);
  color: var(--text-cream);
  padding: 10px 12px;
  font-family: 'DM Sans', sans-serif;
  font-size: .78rem;
  font-weight: 300;
  outline: none;
  transition: border-color .2s ease;
  -webkit-appearance: none;
}

.input-field:focus, .select-field:focus, .textarea-field:focus {
  border-color: var(--brand-gold);
}

.input-field::placeholder, .textarea-field::placeholder {
  color: var(--text-faint);
}

.select-field {
  cursor: pointer;
  appearance: none;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='10' height='6' viewBox='0 0 10 6'%3E%3Cpath fill='%23A8A296' d='M5 6L0 0h10z'/%3E%3C/svg%3E");
  background-repeat: no-repeat;
  background-position: right 12px center;
}

.select-field option {
  background: var(--bg-card);
}

.textarea-field {
  resize: none;
  min-height: 80px;
}

.urgency-toggle-row {
  display: flex;
}

.urgency-btn {
  flex: 1;
  padding: 10px;
  background: var(--bg-card);
  border: 1px solid var(--border-charcoal);
  color: var(--text-placeholder);
  font-family: 'DM Sans', sans-serif;
  font-size: .6rem;
  font-weight: 600;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  cursor: pointer;
  transition: all .2s ease;
}

.urgency-btn:not(:first-child) {
  border-left: none;
}

.urgency-btn.active {
  background: var(--brand-gold);
  color: var(--bg-dark);
  border-color: var(--brand-gold);
}

.form-submit-btn {
  width: 100%;
  background: var(--brand-gold);
  color: var(--bg-dark);
  border: none;
  padding: 14px;
  font-family: 'DM Sans', sans-serif;
  font-size: .68rem;
  font-weight: 700;
  letter-spacing: 2px;
  text-transform: uppercase;
  cursor: pointer;
  transition: background .2s ease;
  margin-top: 12px;
}

.form-submit-btn:hover {
  background: var(--brand-gold-light);
}

.form-submit-btn:disabled {
  opacity: .4;
  cursor: not-allowed;
}

.form-footnote {
  font-size: .62rem;
  color: var(--text-placeholder);
  text-align: center;
  margin-top: 8px;
  letter-spacing: 1px;
  text-transform: uppercase;
}

.form-error {
  display: none;
  font-size: .7rem;
  color: #f87171;
  padding: 10px 12px;
  background: rgba(248, 113, 113, .05);
  border: 1px solid rgba(248, 113, 113, .15);
  margin-top: 10px;
}

.form-success {
  display: none;
  text-align: center;
  padding: 56px 24px;
}

.success-title {
  font-family: 'Fraunces', serif;
  font-size: 1.6rem;
  font-weight: 300;
  font-style: italic;
  color: var(--text-cream);
  margin-bottom: 10px;
}

.success-line {
  width: 32px;
  height: 1px;
  background: var(--brand-gold);
  margin: 14px auto;
}

.success-desc {
  font-size: .8rem;
  font-weight: 400;
  color: var(--text-muted);
  line-height: 1.8;
}

/* ==========================================
   11. CONTACT FOOTPRINT
   ========================================== */
.contact-row-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  border-left: 1px solid var(--border-charcoal);
  border-top: 1px solid var(--border-charcoal);
}

.contact-info-card {
  border-right: 1px solid var(--border-charcoal);
  border-bottom: 1px solid var(--border-charcoal);
  padding: 32px 24px;
  transition: background .15s ease;
}

.contact-info-card:hover {
  background: var(--bg-card);
}

.card-label {
  font-size: .58rem;
  font-weight: 700;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--brand-gold);
  margin-bottom: 10px;
}

.card-value {
  font-size: .88rem;
  font-weight: 600;
  color: var(--text-cream);
  margin-bottom: 3px;
}

.card-value a {
  color: var(--text-cream);
  transition: color .2s ease;
}

.card-value a:hover {
  color: var(--brand-gold);
}

.card-hint {
  font-size: .72rem;
  font-weight: 400;
  color: var(--text-placeholder);
}

/* ==========================================
   12. TRUST & PAYMENT LABELS
   ========================================== */
.payment-ticker {
  background: var(--bg-card);
  border-bottom: 1px solid var(--border-charcoal);
  padding: 15px 6%;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 48px;
  flex-wrap: wrap;
}

.payment-label {
  font-size: .65rem;
  font-weight: 600;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--text-placeholder);
  display: flex;
  align-items: center;
  gap: 7px;
}

.payment-label::before {
  content: '';
  width: 3px;
  height: 3px;
  background: var(--brand-gold);
  border-radius: 50%;
  flex-shrink: 0;
}

/* ==========================================
   13. STRUCTURAL FOOTER
   ========================================== */
footer {
  background: var(--bg-card);
  padding: 52px 6% 28px;
  border-top: 1px solid var(--border-charcoal);
}

.footer-top-layout {
  display: grid;
  grid-template-columns: 1.6fr 1fr;
  gap: 40px;
  padding-bottom: 36px;
  border-bottom: 1px solid var(--border-charcoal);
  margin-bottom: 24px;
}

.footer-brand {
  font-family: 'Fraunces', serif;
  font-size: 1.15rem;
  font-weight: 600;
  color: var(--text-cream);
  margin-bottom: 8px;
  letter-spacing: -.3px;
}

.footer-brand b {
  color: var(--brand-gold);
  font-weight: 600;
}

.footer-tagline {
  font-size: .75rem;
  font-weight: 400;
  color: var(--text-placeholder);
  line-height: 1.75;
}

.footer-heading {
  font-size: .56rem;
  font-weight: 700;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--brand-gold);
  margin-bottom: 14px;
}

.footer-nav-list {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.footer-nav-list li, .footer-nav-list a {
  font-size: .78rem;
  font-weight: 400;
  color: var(--text-placeholder);
  transition: color .2s ease;
}

.footer-nav-list a:hover {
  color: var(--brand-gold);
}

.footer-bottom-layout {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 8px;
}

.footer-copyright {
  font-size: .65rem;
  font-weight: 400;
  color: var(--text-placeholder);
  letter-spacing: .3px;
}

.footer-copyright a:hover {
  color: var(--brand-gold);
}

/* ==========================================
   14. SYSTEM RESPONSIVENESS
   ========================================== */
@media(max-width: 1100px) {
  .fleet-grid {
    grid-template-columns: repeat(2, 1fr);
  }
  .map-layout {
    grid-template-columns: 1fr;
  }
  .map-sidebar {
    border-left: none;
    border-top: 1px solid var(--border-charcoal);
  }
  .estimator-section {
    grid-template-columns: 1fr;
  }
  .quote-layout {
    grid-template-columns: 1fr;
  }
  .contact-row-grid {
    grid-template-columns: 1fr 1fr;
  }
  .footer-top-layout {
    grid-template-columns: 1fr 1fr;
  }
}

/* Accessibilité : focus clavier visible + respect des préférences de mouvement */
a:focus-visible, button:focus-visible, .estimator-select:focus-visible,
.input-field:focus-visible, .textarea-field:focus-visible, .select-field:focus-visible {
  outline: 2px solid var(--brand-gold);
  outline-offset: 2px;
}

@media (prefers-reduced-motion: reduce) {
  html { scroll-behavior: auto; }
  *, *::before, *::after {
    animation-duration: .01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: .01ms !important;
  }
}

@media(max-width: 768px) {
  html { -webkit-text-size-adjust: 100%; }
  .topbar, .nav-links, .nav-tel { display: none; }
  .nav-hamburger { display: flex; }
  .nav-cta { padding: 10px 14px; font-size: .66rem; }
  nav { padding: 0 5%; height: 58px; }

  /* Hero : plus de vide en haut, blocs empilés proprement */
  .hero { min-height: auto; padding: 64px 5% 44px; }
  .hero-bg-text { display: none; }
  .hero-eyebrow { margin-bottom: 22px; gap: 10px; }
  .hero-eyebrow-line { width: 22px; flex-shrink: 0; }
  .hero-eyebrow-txt { font-size: .62rem; letter-spacing: 2px; line-height: 1.6; }
  .hero h1 { font-size: clamp(2.7rem, 13vw, 3.6rem); letter-spacing: -1.5px; line-height: 1; }
  .hero-caption { font-size: .95rem; margin-top: 22px; max-width: none; }
  .hero-actions { flex-direction: column; gap: 10px; margin-top: 28px; }
  .btn-primary, .btn-secondary { width: 100%; text-align: center; padding: 16px 20px; }
  .hero-stats {
    display: grid; grid-template-columns: 1fr 1fr; gap: 26px 20px;
    margin-top: 40px; padding-top: 28px;
  }
  .stat-box, .stat-box:not(:first-child), .stat-box:last-child { border: none; padding: 0; }
  .stat-label { font-size: .64rem; }

  /* Sections */
  .section-header { padding: 48px 5% 28px; }
  .section-desc { font-size: .92rem; }
  .services-row { grid-template-columns: 1fr; }
  .service-meta { padding: 22px 5% 4px; border-right: none; }
  .service-content { padding: 4px 5% 22px; border-right: none; }
  .service-desc { font-size: .88rem; line-height: 1.75; }
  .service-vehicle { display: none; }
  .service-num { font-size: .66rem; }
  .service-name { font-size: 1rem; }

  .fleet-grid { grid-template-columns: 1fr; }
  .feature-item { font-size: .76rem; }
  .vehicle-sub { font-size: .78rem; }
  .vehicle-index { font-size: .62rem; }
  .vehicle-eta { font-size: .7rem; }
  .status-tag { font-size: .58rem; }

  .zone-map-visual { height: 340px; }
  .zone-map-caption { display: none; }
  .zone-map-svg .dept-label.zone-1, .zone-map-svg .dept-label.zone-2 { font-size: 17px; }
  .zone-map-svg .dept-label.zone-3 { font-size: 18px; }
  .zone-details, .quick-contact-text { font-size: .8rem; }

  /* Simulateur & formulaire : cibles tactiles confortables, pas de zoom iOS */
  .estimator-section { padding: 48px 5%; gap: 32px; }
  .estimator-label, .form-label { font-size: .68rem; }
  .estimator-select, .estimator-input, .input-field, .select-field, .textarea-field {
    font-size: 16px; min-height: 48px; padding-top: 12px; padding-bottom: 12px;
  }
  .textarea-field { min-height: 110px; }
  .urgency-btn { min-height: 48px; font-size: .66rem; padding: 0 6px; }
  .estimator-button, .form-submit-btn { min-height: 52px; }
  .estimator-note, .form-footnote { font-size: .72rem; }

  .quote-sidebar, .quote-content { padding: 40px 5%; }
  .form-grid { grid-template-columns: 1fr; gap: 0; }
  .form-group, .form-group:last-child, .form-grid .form-group:last-child { margin-bottom: 16px; }
  .form-header-sub { font-size: .74rem; }
  .direct-hours { font-size: .74rem; }
  .direct-label { font-size: .64rem; }
  .promise-text { font-size: .86rem; }
  .form-header-title { font-size: .95rem; }

  /* Contact & pied de page */
  .contact-row-grid { grid-template-columns: 1fr; }
  .card-label { font-size: .64rem; }
  .card-hint { font-size: .78rem; }
  .footer-top-layout { grid-template-columns: 1fr; gap: 28px; }
  .footer-nav-list li, .footer-nav-list a { font-size: .86rem; }
  .footer-nav-list a { display: inline-block; padding: 3px 0; }
  .footer-tagline { font-size: .84rem; }
  .footer-bottom-layout { flex-direction: column; gap: 8px; align-items: flex-start; }
  .footer-copyright { font-size: .72rem; }
}

/* ==========================================
   15. MOBILE VISUAL POLISH
   Palette volontairement plus sobre sur téléphone
   ========================================== */
@media(max-width: 768px) {
  :root {
    --brand-gold: #C8A45D;
    --brand-gold-light: #D7B875;
    --brand-gold-dark: #8F733E;
    --bg-dark: #111315;
    --bg-card: #191C1F;
    --bg-input: #202428;
    --border-charcoal: #2D3237;
    --border-light: #3A4046;
    --text-muted: #B8BDC2;
    --text-placeholder: #8D949B;
    --text-faint: #687078;
    --text-cream: #F5F5F3;
    --text-warm-white: #E6E7E5;
  }

  body { background: #111315; color: #F5F5F3; }
  nav { background: rgba(17,19,21,.96); border-bottom: 1px solid #2D3237; }
  .nav-logo, .nav-logo b, .hero h1, .section-title, .service-name,
  .form-header-title, .footer-brand, .footer-brand b { color: #F5F5F3 !important; }

  /* L'or devient un accent, pas une couleur dominante. */
  .hero-eyebrow-txt, .service-num, .card-label, .footer-heading,
  .estimator-label, .form-label, .direct-label { color: #C8A45D !important; }

  .btn-primary, .estimator-button, .form-submit-btn {
    background: #C8A45D !important;
    color: #111315 !important;
    border-color: #C8A45D !important;
    box-shadow: none !important;
  }

  .btn-secondary {
    background: #191C1F !important;
    color: #F5F5F3 !important;
    border: 1px solid #3A4046 !important;
  }

  .service-content, .service-meta, .contact-info-card, .quote-sidebar,
  .quote-content, .fleet-card, .estimator-section, .map-sidebar {
    background: #191C1F;
    border-color: #2D3237;
  }

  .service-row, .contact-info-card, .fleet-card {
    box-shadow: 0 8px 24px rgba(0,0,0,.18);
  }

  .hero {
    background: linear-gradient(180deg, #111315 0%, #15181B 100%);
  }

  .hero-caption, .section-desc, .service-desc, .card-hint,
  .footer-tagline, .promise-text { color: #B8BDC2 !important; }

  .urgency-btn {
    background: #191C1F !important;
    border-color: #3A4046 !important;
    color: #D9DCDD !important;
  }
  .urgency-btn.active {
    background: rgba(200,164,93,.12) !important;
    border-color: #C8A45D !important;
    color: #D7B875 !important;
  }

  .input-field, .select-field, .textarea-field, .estimator-select, .estimator-input {
    background: #202428 !important;
    border-color: #343A40 !important;
    color: #F5F5F3 !important;
  }

  .footer-bottom-layout { border-top-color: #2D3237 !important; }
}

@media(max-width: 480px) {
  .estimator-row { grid-template-columns: 1fr; }
}

@media(max-width: 380px) {
  .hero-eyebrow-txt { letter-spacing: 1.4px; }
  .nav-logo { font-size: 1.1rem; }
  .nav-cta { padding: 9px 11px; }
  .urgency-btn { font-size: .6rem; letter-spacing: 0; }
  .estimator-row { grid-template-columns: 1fr; }
}

/* ==========================================
   16. MOBILE COMPACT MODE — Toute Solution
   Réduit les gros blocs et garde l'or uniquement en accent.
   ========================================== */
@media (max-width: 768px) {
  body { overflow-x:hidden; }
  .section-wrapper { padding-left:4%; padding-right:4%; }
  nav { height:54px; padding:0 4%; }
  .nav-logo { font-size:1.02rem !important; }
  .nav-cta { padding:8px 10px !important; font-size:.58rem !important; }

  .hero { padding:42px 4% 30px !important; }
  .hero h1 { font-size:clamp(2.05rem, 10vw, 2.8rem) !important; }
  .hero-caption { font-size:.82rem !important; line-height:1.55; margin-top:14px !important; }
  .hero-eyebrow { margin-bottom:14px !important; }
  .hero-actions { gap:8px !important; margin-top:18px !important; }
  .btn-primary, .btn-secondary { padding:11px 14px !important; font-size:.68rem !important; }
  .hero-stats { gap:16px 12px !important; margin-top:25px !important; padding-top:18px !important; }
  .stat-label { font-size:.56rem !important; }

  .section-header { padding:32px 4% 20px !important; }
  .section-title { font-size:1.55rem !important; }
  .section-desc { font-size:.78rem !important; line-height:1.55 !important; }

  .service-row, .fleet-card, .contact-info-card, .quote-sidebar,
  .quote-content, .estimator-section, .map-sidebar, .zone-quick-contact,
  .form-wrapper, .direct-contact-card {
    border-radius:8px !important;
  }

  .service-meta { padding:14px 4% 3px !important; }
  .service-content { padding:3px 4% 15px !important; }
  .service-name { font-size:.88rem !important; }
  .service-desc { font-size:.74rem !important; line-height:1.55 !important; }
  .service-num { font-size:.56rem !important; }

  .fleet-card { padding:14px !important; }
  .feature-item { font-size:.66rem !important; }
  .vehicle-sub { font-size:.68rem !important; }
  .vehicle-index, .status-tag { font-size:.54rem !important; }

  .zone-map-visual { height:250px !important; }
  .zones-summary-left { padding:28px 4% !important; }
  .zone-info { padding:10px 12px !important; }
  .zone-name { font-size:.68rem !important; }
  .zone-details { font-size:.62rem !important; }
  .zone-quick-contact { margin-top:10px !important; padding:11px !important; }
  .quick-contact-text { font-size:.62rem !important; margin-bottom:6px !important; }
  .quick-contact-phone { font-size:.76rem !important; }

  .estimator-section { padding:28px 4% !important; gap:20px !important; }
  .estimator-label, .form-label { font-size:.58rem !important; }
  .estimator-select, .estimator-input, .input-field, .select-field, .textarea-field {
    min-height:42px !important; font-size:14px !important; padding:9px 11px !important;
  }
  .textarea-field { min-height:85px !important; }
  .urgency-btn { min-height:40px !important; font-size:.58rem !important; }
  .estimator-button, .form-submit-btn { min-height:44px !important; font-size:.66rem !important; }

  /* Bloc téléphone/e-mail : compact, sombre, or seulement en détail. */
  .direct-contact-card {
    margin-top:12px !important;
    padding:13px 14px !important;
    background:#191C1F !important;
    color:#F5F5F3 !important;
    border:1px solid #343A40 !important;
    border-left:3px solid #C8A45D !important;
  }
  .direct-label { font-size:.5rem !important; letter-spacing:1.8px !important; margin-bottom:5px !important; color:#C8A45D !important; opacity:1 !important; }
  .direct-phone { font-size:1.02rem !important; margin-bottom:2px !important; color:#F5F5F3 !important; }
  .direct-email { font-size:.63rem !important; color:#B8BDC2 !important; opacity:1 !important; }
  .direct-hours { font-size:.54rem !important; margin-top:4px !important; color:#8D949B !important; opacity:1 !important; }

  .form-header {
    padding:11px 13px !important;
    background:#191C1F !important;
    color:#F5F5F3 !important;
    border-bottom:1px solid #343A40 !important;
    border-left:3px solid #C8A45D !important;
  }
  .form-header-title { font-size:.72rem !important; color:#F5F5F3 !important; }
  .form-header-sub { font-size:.54rem !important; color:#8D949B !important; }
  .form-body { padding:14px !important; }
  .form-group { margin:9px auto !important; gap:4px !important; background:transparent !important; }
  .form-footnote, .estimator-note { font-size:.58rem !important; }

  /* Toutes les cartes de contact : petites et cohérentes. */
  .contact-row-grid { gap:7px !important; border:0 !important; }
  .contact-info-card {
    padding:13px 14px !important;
    border:1px solid #2D3237 !important;
    background:#191C1F !important;
    box-shadow:none !important;
  }
  .card-label { font-size:.52rem !important; letter-spacing:1.6px !important; margin-bottom:5px !important; }
  .card-value { font-size:.76rem !important; margin-bottom:2px !important; }
  .card-hint { font-size:.61rem !important; line-height:1.35 !important; }

  .promise-row { min-height:0 !important; }
  .promise-index { min-width:30px !important; padding:9px !important; font-size:.54rem !important; }
  .promise-text { padding:9px 10px !important; font-size:.64rem !important; }

  .footer-top-layout { gap:18px !important; }
  .footer-tagline { font-size:.68rem !important; line-height:1.5 !important; }
  .footer-nav-list li, .footer-nav-list a { font-size:.68rem !important; }
  .footer-copyright { font-size:.56rem !important; }
}

@media (max-width: 480px) {
  .hero { padding-top:34px !important; }
  .hero h1 { font-size:2rem !important; }
  .section-title { font-size:1.38rem !important; }
  .section-header { padding-top:27px !important; padding-bottom:17px !important; }
  .direct-contact-card { padding:11px 12px !important; }
  .contact-info-card { padding:11px 12px !important; }
}

</style>

<style id="toute-solution-production-polish">
/* =========================================================
   PRODUCTION POLISH — Toute Solution
   Objectif : rendu premium, lisible et réellement responsive.
   ========================================================= */
:root{
  --brand-gold:#D2AD62;
  --brand-gold-light:#E4C47E;
  --brand-gold-dark:#9D7B38;
  --bg-dark:#0B1116;
  --bg-card:#111920;
  --bg-input:#172027;
  --border-charcoal:#25313A;
  --border-light:#34414B;
  --text-muted:#AEB7BE;
  --text-placeholder:#7F8A92;
  --text-faint:#657079;
  --text-cream:#F4F6F7;
  --text-warm-white:#E8ECEE;
}
html{background:var(--bg-dark);}
body{background:linear-gradient(180deg,#0B1116 0%,#0D141A 45%,#0A1015 100%);color:var(--text-cream);}
::selection{background:rgba(210,173,98,.28);color:#fff;}

/* Navigation */
nav{background:rgba(11,17,22,.92);backdrop-filter:blur(14px);-webkit-backdrop-filter:blur(14px);border-bottom:1px solid rgba(210,173,98,.16);}
.nav-logo{letter-spacing:-.7px;}
.nav-logo b{color:var(--brand-gold);}
.nav-links a:hover{color:#fff;border-bottom-color:var(--brand-gold);}
.nav-cta{border-radius:7px;box-shadow:0 7px 20px rgba(210,173,98,.12);}

/* Hero */
.hero{background:
  radial-gradient(circle at 78% 22%,rgba(210,173,98,.10),transparent 28%),
  radial-gradient(circle at 18% 65%,rgba(44,92,116,.10),transparent 32%),
  linear-gradient(135deg,#0B1116 0%,#101820 58%,#0A1015 100%);}
.hero h1{letter-spacing:-2.5px;}
.hero h1 em{color:var(--brand-gold-light);}
.hero-caption{color:#B8C0C5;}
.btn-primary{border-radius:8px;box-shadow:0 10px 26px rgba(210,173,98,.15);}
.btn-primary:hover{background:var(--brand-gold-light);transform:translateY(-1px);}
.btn-secondary{border-radius:8px;background:rgba(255,255,255,.025);}
.btn-secondary:hover{border-color:var(--brand-gold);background:rgba(210,173,98,.06);}

/* Cards / sections */
.section-wrapper{position:relative;}
.service-row,.fleet-card,.contact-info-card,.quote-sidebar,.quote-content,.estimator-section,.map-sidebar,.form-wrapper,.direct-contact-card{
  background:linear-gradient(145deg,rgba(17,25,32,.96),rgba(13,20,26,.96));
  border-color:rgba(255,255,255,.08);
  box-shadow:0 12px 34px rgba(0,0,0,.18);
}
.service-row:hover,.fleet-card:hover,.contact-info-card:hover{border-color:rgba(210,173,98,.32);transform:translateY(-2px);transition:.22s ease;}
.card-label,.footer-heading,.estimator-label,.form-label,.direct-label{color:var(--brand-gold);}
.card-value{color:#F4F6F7;}

/* Inputs */
.input-field,.select-field,.textarea-field,.estimator-select,.estimator-input{
  background:#121A21!important;border:1px solid #2A3740!important;color:#F4F6F7!important;border-radius:8px!important;
}
.input-field:focus,.select-field:focus,.textarea-field:focus,.estimator-select:focus,.estimator-input:focus{
  border-color:var(--brand-gold)!important;box-shadow:0 0 0 3px rgba(210,173,98,.10)!important;
}
.form-submit-btn,.estimator-button{border-radius:8px!important;box-shadow:0 10px 24px rgba(210,173,98,.12)!important;}

/* Footer */
footer{background:#090F14;border-top:1px solid rgba(255,255,255,.07);}
.footer-copyright{color:#77828A;}

/* Touch + media safety */
img,svg,video,canvas{max-width:100%;height:auto;}
button,a,.nav-hamburger,.urgency-btn{touch-action:manipulation;}

@media (max-width:768px){
  body{font-size:15px;}
  nav{height:56px;padding:0 4%;}
  .nav-logo{font-size:1rem!important;}
  .nav-cta{padding:8px 11px!important;font-size:.58rem!important;border-radius:6px;}
  .nav-hamburger{width:40px;height:40px;}

  /* Mobile : pas de gros aplats, uniquement des accents. */
  .hero{min-height:auto!important;padding:34px 5% 28px!important;background:
    radial-gradient(circle at 90% 15%,rgba(210,173,98,.08),transparent 30%),
    linear-gradient(160deg,#0B1116,#101820 60%,#0B1116)!important;}
  .hero h1{font-size:clamp(2rem,10vw,2.65rem)!important;line-height:1.02!important;letter-spacing:-1.5px!important;}
  .hero-caption{font-size:.82rem!important;line-height:1.55!important;}
  .hero-actions{display:grid!important;grid-template-columns:1fr 1fr;gap:8px!important;}
  .btn-primary,.btn-secondary{min-height:42px!important;padding:10px 12px!important;font-size:.67rem!important;}
  .hero-stats{gap:10px!important;margin-top:20px!important;padding-top:15px!important;}
  .stat-label{font-size:.55rem!important;line-height:1.35!important;}

  .section-header{padding:28px 5% 16px!important;}
  .section-title{font-size:1.45rem!important;line-height:1.12!important;}
  .section-desc{font-size:.76rem!important;line-height:1.5!important;}

  .service-row,.fleet-card,.contact-info-card,.quote-sidebar,.quote-content,.estimator-section,.map-sidebar,.form-wrapper,.direct-contact-card{
    border-radius:9px!important;box-shadow:0 8px 22px rgba(0,0,0,.16)!important;
  }
  .service-row:hover,.fleet-card:hover,.contact-info-card:hover{transform:none;}
  .service-content{padding:3px 4% 13px!important;}
  .service-meta{padding:12px 4% 3px!important;}
  .service-name{font-size:.88rem!important;}
  .service-desc{font-size:.73rem!important;line-height:1.5!important;}

  .contact-row-grid{gap:9px!important;}
  .contact-info-card{padding:13px!important;}
  .card-label{font-size:.56rem!important;letter-spacing:1.2px!important;}
  .card-value{font-size:.84rem!important;word-break:break-word;}
  .card-hint{font-size:.62rem!important;}

  .estimator-section{padding:24px 5%!important;gap:16px!important;}
  .estimator-select,.estimator-input,.input-field,.select-field,.textarea-field{min-height:42px!important;font-size:14px!important;padding:9px 11px!important;}
  .textarea-field{min-height:82px!important;}
  .urgency-btn{min-height:39px!important;font-size:.57rem!important;border-radius:7px!important;}
  .estimator-button,.form-submit-btn{min-height:44px!important;}

  .zone-map-visual{height:210px!important;}
  .zones-summary-left{padding:24px 5%!important;}
  footer{padding:36px 5% 24px!important;}
  .footer-top-layout{gap:24px!important;}
}

@media (max-width:480px){
  .hero-actions{grid-template-columns:1fr!important;}
  .hero-eyebrow{margin-bottom:12px!important;}
  .hero-eyebrow-txt{font-size:.58rem!important;letter-spacing:1.6px!important;}
  .contact-row-grid{grid-template-columns:1fr!important;}
  .footer-top-layout{grid-template-columns:1fr!important;}
}

@media (max-width:380px){
  .hero{padding-left:4.5%!important;padding-right:4.5%!important;}
  .hero h1{font-size:1.9rem!important;}
  .section-header{padding-left:4.5%!important;padding-right:4.5%!important;}
  .nav-cta{display:none;}
}

@media (prefers-reduced-motion:reduce){
  *,*::before,*::after{scroll-behavior:auto!important;animation:none!important;transition:none!important;}
}
</style>

</head>
<body>

<!-- TOPBAR SYSTEM STATUS -->
<div class="topbar">
  <span class="topbar-left">Service 24h/24 — 7j/7 · Paris & Île-de-France</span>
  <div class="topbar-right">
    <a href="mailto:Toutesolution.75@gmail.com">Toutesolution.75@gmail.com</a>
    <a href="tel:0774800964">07 74 80 09 64</a>
  </div>
</div>

<!-- STICKY NAVIGATION -->
<nav>
  <div class="nav-logo">Toute<b>Solution</b></div>
  <ul class="nav-links">
    <li><a href="#services">Services</a></li>
    <li><a href="#fleet">Véhicules</a></li>
    <li><a href="#devis">Devis</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <div class="nav-actions">
    <a href="tel:0774800964" class="nav-tel">07 74 80 09 64</a>
    <a href="#devis" class="nav-cta">Devis gratuit</a>
    <button type="button" class="nav-hamburger" id="nav-hamburger" aria-label="Ouvrir le menu" aria-expanded="false">
      <span></span><span></span><span></span>
    </button>
  </div>
</nav>

<div class="mobile-menu" id="mobile-menu">
  <ul>
    <li><a href="#services">Services</a></li>
    <li><a href="#fleet">Véhicules</a></li>
    <li><a href="#devis">Devis</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <div class="mobile-menu-contact">
    <a href="tel:0774800964">07 74 80 09 64</a>
    <a href="mailto:Toutesolution.75@gmail.com">Toutesolution.75@gmail.com</a>
  </div>
  <a href="#devis" class="mobile-menu-cta">Devis gratuit</a>
</div>

<!-- HERO SCREEN -->
<section class="hero">
  <div class="hero-line"></div>
  <div class="hero-bg-text">Express</div>
  <div class="hero-content">
    <div class="hero-eyebrow">
      <div class="hero-eyebrow-line"></div>
      <div class="hero-eyebrow-txt">Paris & Île-de-France — Disponible 24h/24</div>
    </div>
    <h1><em>Livraison</em><br><strong>express</strong> &<br>déménagement.</h1>
    <p class="hero-caption">Rapide, sérieux, efficace. Notre flotte intervient partout à Paris et en Île-de-France, jour et nuit, 7 jours sur 7.</p>
    <div class="hero-actions">
      <a href="#devis" class="btn-primary">Demander un devis gratuit</a>
      <a href="tel:0774800964" class="btn-secondary">07 74 80 09 64</a>
    </div>
    <div class="hero-stats">
      <div class="stat-box"><div class="stat-value">24/7</div><div class="stat-label">Disponibilité</div></div>
      <div class="stat-box"><div class="stat-value">45'</div><div class="stat-label">Délai moyen</div></div>
      <div class="stat-box"><div class="stat-value">4</div><div class="stat-label">Véhicules</div></div>
      <div class="stat-box"><div class="stat-value">IDF</div><div class="stat-label">Zone couverte</div></div>
    </div>
  </div>
</section>

<!-- SERVICES SECTION -->
<section class="section-wrapper" id="services">
  <div class="section-header">
    <div class="section-eyebrow"><div class="section-eyebrow-line"></div><div class="section-kicker">Nos prestations</div></div>
    <h2 class="section-title">Tous vos besoins,<br><em>un seul numéro.</em></h2>
    <p class="section-desc">Course urgente ou déménagement complet — nous avons le véhicule et le service adaptés à chaque situation.</p>
  </div>
  
  <div class="services-table">
    <div class="services-row">
      <div class="service-meta">
        <div class="service-num">01</div>
        <div class="service-name">Course & Livraison</div>
      </div>
      <div class="service-content">
        <p class="service-desc">Courses et achats à votre place · Colis et documents · Récupération de clés et d'objets · Retours de colis</p>
      </div>
      <div class="service-vehicle">
        <div class="vehicle-badge">Moto</div>
      </div>
    </div>
    
    <div class="services-row">
      <div class="service-meta">
        <div class="service-num">02</div>
        <div class="service-name">Transport colis</div>
      </div>
      <div class="service-content">
        <p class="service-desc">Livraison toutes tailles · Remise en main propre · Envois urgents nuit et jour · Documents, lettres, contrats</p>
      </div>
      <div class="service-vehicle">
        <div class="vehicle-badge">Moto<br>Voiture</div>
      </div>
    </div>
    
    <div class="services-row">
      <div class="service-meta">
        <div class="service-num">03</div>
        <div class="service-name">Déménagement</div>
      </div>
      <div class="service-content">
        <p class="service-desc">Studios, appartements, bureaux · Mobilier et objets encombrants · Manutention disponible · Hayon élévateur · Grand Paris et Île-de-France</p>
      </div>
      <div class="service-vehicle">
        <div class="vehicle-badge">Camion<br>12m³ / 20m³</div>
      </div>
    </div>
    
    <div class="services-row">
      <div class="service-meta">
        <div class="service-num">04</div>
        <div class="service-name">Urgences 24h/24</div>
      </div>
      <div class="service-content">
        <p class="service-desc">Nuit, week-end, jours fériés · Médicaments et pharmacie · Documents et clés urgents · Intervention en moins d'une heure dans Paris</p>
      </div>
      <div class="service-vehicle">
        <div class="vehicle-badge">Tous<br>véhicules</div>
      </div>
    </div>
  </div>
</section>

<!-- VEHICLE FLEET SECTION -->
<section class="section-wrapper fleet-section" id="fleet">
  <div class="section-header">
    <div class="section-eyebrow"><div class="section-eyebrow-line"></div><div class="section-kicker">Notre flotte</div></div>
    <h2 class="section-title">4 véhicules<br><em>pour chaque mission.</em></h2>
    <p class="section-desc">Chaque véhicule est entretenu et prêt à intervenir. Nous choisissons le plus adapté à votre besoin.</p>
  </div>
  
  <div class="fleet-grid">
    <div class="vehicle-card premium">
      <div class="status-tag on-demand">Disponible sur demande</div>
      <div class="vehicle-icon-wrap">
        <svg viewBox="0 0 64 40" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round">
          <circle cx="14" cy="30" r="7"/><circle cx="50" cy="30" r="7"/>
          <path d="M14 30h14l8-16h10M32 14l6 10M20 30l6-9 10 3M40 14h6l3 6"/>
        </svg>
      </div>
      <div class="vehicle-index">01 — Grande capacité</div>
      <h3 class="vehicle-title">Moto grande capacité<span class="reco-badge">Recommandé</span></h3>
      <p class="vehicle-sub">Multi-livraisons · Paris & banlieue</p>
      <div class="card-divider"></div>
      <div class="vehicle-features">
        <div class="feature-item">Top case et grandes sacoches</div>
        <div class="feature-item">Multi-livraisons simultanées</div>
        <div class="feature-item">Paris et petite couronne</div>
        <div class="feature-item">Courses et colis en volume</div>
      </div>
      <div class="vehicle-eta">Normal 3h · Urgent 1h30 · <b>Super 45min</b></div>
    </div>
    
    <div class="vehicle-card">
      <div class="status-tag">Disponible</div>
      <div class="vehicle-icon-wrap">
        <svg viewBox="0 0 64 40" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round">
          <path d="M6 28V18a3 3 0 0 1 3-3h6l6-7h20l8 7h6a3 3 0 0 1 3 3v10"/>
          <path d="M6 28h52"/><circle cx="16" cy="28" r="5"/><circle cx="48" cy="28" r="5"/>
        </svg>
      </div>
      <div class="vehicle-index">02 — Transport</div>
      <h3 class="vehicle-title">Voiture utilitaire</h3>
      <p class="vehicle-sub">Volumétrique · IDF</p>
      <div class="card-divider"></div>
      <div class="vehicle-features">
        <div class="feature-item">Meubles et objets encombrants</div>
        <div class="feature-item">Grand coffre et capacité volume</div>
        <div class="feature-item">Paris et Île-de-France</div>
        <div class="feature-item">Manutention sur demande</div>
      </div>
      <div class="vehicle-eta">Normal 3h · Urgent 2h · <b>Super 1h30</b></div>
    </div>
    
    <div class="vehicle-card">
      <div class="status-tag">Disponible</div>
      <div class="vehicle-icon-wrap">
        <svg viewBox="0 0 64 40" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round">
          <rect x="4" y="10" width="30" height="18" rx="1"/>
          <path d="M34 16h12l10 7v5H34z"/>
          <circle cx="16" cy="30" r="5"/><circle cx="46" cy="30" r="5"/>
          <path d="M4 30h6M52 30h6"/>
        </svg>
      </div>
      <div class="vehicle-index">03 — Déménagement</div>
      <h3 class="vehicle-title">Camion 12m³</h3>
      <p class="vehicle-sub">Volume moyen · Grand Paris</p>
      <div class="card-divider"></div>
      <div class="vehicle-features">
        <div class="feature-item">Studio et appartement 2 pièces</div>
        <div class="feature-item">Mobilier professionnel</div>
        <div class="feature-item">Tout le Grand Paris</div>
        <div class="feature-item">Manutention incluse</div>
      </div>
      <div class="vehicle-eta"><b>Sur rendez-vous</b></div>
    </div>
    
    <div class="vehicle-card">
      <div class="status-tag soon">Bientôt disponible</div>
      <div class="vehicle-icon-wrap">
        <svg viewBox="0 0 64 40" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round">
          <rect x="2" y="8" width="34" height="20" rx="1"/>
          <path d="M36 15h13l11 8v5H36z"/>
          <circle cx="15" cy="30" r="5"/><circle cx="48" cy="30" r="5"/>
          <path d="M2 30h7M55 30h7"/>
        </svg>
      </div>
      <div class="vehicle-index">04 — Grand volume</div>
      <h3 class="vehicle-title">Camion 20m³</h3>
      <p class="vehicle-sub">Grand volume · IDF</p>
      <div class="card-divider"></div>
      <div class="vehicle-features">
        <div class="feature-item">Grands appartements et maisons</div>
        <div class="feature-item">Bureaux professionnels</div>
        <div class="feature-item">IDF et longue distance</div>
        <div class="feature-item">Hayon élévateur disponible</div>
      </div>
      <div class="vehicle-eta"><b>Sur rendez-vous</b></div>
    </div>
  </div>
</section>

<!-- LIVE FARE ESTIMATOR -->
<section class="estimator-section">
  <div>
    <div class="section-eyebrow" style="margin-bottom:12px">
      <div class="section-eyebrow-line"></div>
      <div class="section-kicker">Estimation tarifaire</div>
    </div>
    <h2 class="section-title" style="font-size:clamp(1.5rem,2.5vw,2.2rem)">Estimez le tarif<br><em>de votre course.</em></h2>
    <p class="section-desc" style="font-size:.78rem; max-width:360px; margin-top:12px">Cette estimation instantanée vous donne un ordre d'idée de prix. Le tarif définitif est systématiquement confirmé par téléphone avant intervention.</p>
  </div>
  
  <div>
    <div class="form-group">
      <label class="estimator-label">Véhicule requis</label>
      <select class="estimator-select" id="est-vehicle" aria-label="Choisir un véhicule">
        <option value="" selected disabled>Choisir un véhicule ▾</option>
        <option value="moto2">Moto grande capacité</option>
        <option value="voiture">Voiture utilitaire</option>
        <option value="camion12">Camion 12m³</option>
        <option value="camion20" disabled>Camion 20m³ (bientôt disponible)</option>
      </select>
      <div class="select-options-hint">Options : Moto grande capacité · Voiture utilitaire · Camion 12m³</div>
      <div class="field-error" id="vehicle-error">Sélectionnez un véhicule pour lancer l'estimation.</div>
    </div>
    
    <div class="estimator-row">
      <div class="form-group">
        <label class="estimator-label">Départ (Département)</label>
        <select class="estimator-select" id="est-pickup" aria-label="Choisir le département de départ">
          <option value="75" selected>75 - Paris ▾</option>
          <option value="92">92 - Hauts-de-Seine</option>
          <option value="93">93 - Seine-Saint-Denis</option>
          <option value="94">94 - Val-de-Marne</option>
          <option value="77">77 - Seine-et-Marne</option>
          <option value="78">78 - Yvelines</option>
          <option value="91">91 - Essonne</option>
          <option value="95">95 - Val-d'Oise</option>
          <option value="other">Autre / Hors IDF</option>
        </select>
      </div>
      <div class="form-group">
        <label class="estimator-label">Arrivée (Département)</label>
        <select class="estimator-select" id="est-delivery" aria-label="Choisir le département d'arrivée">
          <option value="75" selected>75 - Paris ▾</option>
          <option value="92">92 - Hauts-de-Seine</option>
          <option value="93">93 - Seine-Saint-Denis</option>
          <option value="94">94 - Val-de-Marne</option>
          <option value="77">77 - Seine-et-Marne</option>
          <option value="78">78 - Yvelines</option>
          <option value="91">91 - Essonne</option>
          <option value="95">95 - Val-d'Oise</option>
          <option value="other">Autre / Hors IDF</option>
        </select>
      </div>
    </div>
    
    <div class="form-group">
      <label class="estimator-label">Niveau d'urgence</label>
      <div class="urgency-toggle-row" id="urgency-selector">
        <button type="button" class="urgency-btn active" data-urgency="normal">Normal</button>
        <button type="button" class="urgency-btn" data-urgency="urgent">Urgent</button>
        <button type="button" class="urgency-btn" data-urgency="super">Super Urgent</button>
      </div>
    </div>
    
    <button type="button" class="estimator-button" id="btn-estimate">Calculer l'estimation</button>
    
    <div class="estimator-result" id="estimate-result-box">
      <div class="estimator-price" id="estimated-price">0,00 €</div>
      <div class="estimator-note">Tarif HT indicatif (hors majoration spécifique de nuit, week-end, attente sur place ou manutention lourde).</div>
    </div>
  </div>
</section>

<!-- QUOTE & CUSTOM REQUEST FORM -->
<section class="section-wrapper" id="devis">
  <div class="quote-layout">
    <div class="quote-sidebar">
      <div class="section-kicker" style="margin-bottom:15px">Demander un devis</div>
      <h3 style="font-family:'Fraunces',serif; font-size:1.8rem; font-weight:300; line-height:1.2; margin-bottom:20px;">Votre étude personnalisée</h3>
      <p style="font-size:0.75rem; color:var(--text-muted); line-height:1.6; margin-bottom:30px;">Pour des transports planifiés, réguliers ou des déménagements plus complets, nos conseillers vous proposent une offre sur mesure.</p>

      <div class="promise-list">
        <div class="promise-row">
          <div class="promise-index">01</div>
          <div class="promise-text">Zéro frais masqué, engagement tarifaire transparent.</div>
        </div>
        <div class="promise-row">
          <div class="promise-index">02</div>
          <div class="promise-text">Chauffeurs professionnels formés et qualifiés.</div>
        </div>
        <div class="promise-row">
          <div class="promise-index">03</div>
          <div class="promise-text">Matériel de transport pro et arrimage sécurisé.</div>
        </div>
      </div>

    </div>

    <div class="quote-content">
      <div class="form-wrapper">
        <div class="form-header">
          <div>
            <div class="form-header-title">Formulaire de demande de devis</div>
            <div class="form-header-sub">Réponse rapide garantie</div>
          </div>
        </div>
        
        <form class="form-body" id="quote-request-form">
          <input type="hidden" name="_subject" value="Nouvelle demande de devis — TouteSolution">
          <input type="text" name="_honey" style="display:none" tabindex="-1" autocomplete="off">
          <div class="form-grid">
            <div class="form-group">
              <label class="form-label">Nom Complet *</label>
              <input type="text" class="input-field" placeholder="Ex: Thomas Martin" required id="form-name" name="Nom complet">
            </div>
            <div class="form-group">
              <label class="form-label">Téléphone *</label>
              <input type="tel" class="input-field" placeholder="Ex: 06 12 34 56 78" required id="form-phone" name="Téléphone">
            </div>
          </div>

          <div class="form-group">
            <label class="form-label">Adresse E-mail *</label>
            <input type="email" class="input-field" placeholder="Ex: t.martin@example.com" required id="form-email" name="Email">
          </div>

          <div class="form-grid">
            <div class="form-group">
              <label class="form-label">Adresse de départ *</label>
              <input type="text" class="input-field" placeholder="Adresse complète" required id="form-pickup" name="Adresse de départ">
            </div>
            <div class="form-group">
              <label class="form-label">Adresse d'arrivée *</label>
              <input type="text" class="input-field" placeholder="Adresse complète" required id="form-delivery" name="Adresse d'arrivée">
            </div>
          </div>

          <div class="form-grid">
            <div class="form-group">
              <label class="form-label">Prestation souhaitée *</label>
              <select class="select-field" required id="form-service" name="Prestation" aria-label="Choisir une prestation">
                <option value="course" selected>Course urgente / Plis ▾</option>
                <option value="colis">Livraison de colis volumineux</option>
                <option value="demenagement">Petit déménagement / Transport meuble</option>
              </select>
              <div class="select-options-hint">Options : Course urgente / Plis · Livraison de colis volumineux · Petit déménagement</div>
            </div>
            <div class="form-group">
              <label class="form-label">Volume ou Poids approx.</label>
              <input type="text" class="input-field" placeholder="Ex: 5 cartons, 45kg" id="form-load" name="Volume / Poids">
            </div>
          </div>

          <div class="form-group">
            <label class="form-label">Précisions (étages, ascenseur, contraintes, etc.)</label>
            <textarea class="textarea-field" placeholder="Détaillez au mieux votre demande pour obtenir un prix précis..." id="form-notes" name="Précisions"></textarea>
          </div>

          <button type="submit" class="form-submit-btn" id="btn-submit">Envoyer ma demande</button>
          <div class="form-footnote">Réponse sous 15 minutes en journée · Données confidentielles</div>

          <div class="form-error" id="form-error-banner">Erreur de connexion. Veuillez réessayer ou nous contacter par téléphone au 07 74 80 09 64.</div>
        </form>

        <div class="form-success" id="form-success-banner">
          <div class="success-title">Demande reçue !</div>
          <div class="success-line"></div>
          <p class="success-desc">Votre demande a été transmise avec succès à notre répartiteur. Un devis définitif ou une confirmation de tarif vous sera communiqué par téléphone ou par e-mail dans les plus brefs délais.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT GRID FOOTPRINT -->
<section class="section-wrapper" id="contact">
  <div class="contact-row-grid">
    <div class="contact-info-card">
      <div class="card-label">Téléphone</div>
      <div class="card-value"><a href="tel:0774800964">07 74 80 09 64</a></div>
      <div class="card-hint">Ligne directe, appel ou SMS</div>
    </div>
    <div class="contact-info-card">
      <div class="card-label">Adresse E-mail</div>
      <div class="card-value"><a href="mailto:Toutesolution.75@gmail.com">Toutesolution.75@gmail.com</a></div>
      <div class="card-hint">Pour vos devis écrits & factures</div>
    </div>
    <div class="contact-info-card">
      <div class="card-label">Zone d'intervention</div>
      <div class="card-value">Paris & Île-de-France</div>
      <div class="card-hint">Départ national possible sur devis</div>
    </div>
    <div class="contact-info-card">
      <div class="card-label">Disponibilité</div>
      <div class="card-value">24h/24 — 7j/7</div>
      <div class="card-hint">Tarifs majorés de nuit (22h - 6h)</div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-top-layout">
    <div>
      <div class="footer-brand">Toute<b>Solution</b></div>
      <p class="footer-tagline">Service de coursiers et de déménagement professionnels opérant sans interruption en région parisienne. Fiabilité éprouvée, réactivité immédiate.</p>
    </div>
    <div>
      <div class="footer-heading">Nos Services</div>
      <ul class="footer-nav-list">
        <li><a href="#services">Course express</a></li>
        <li><a href="#services">Livraison colis lourd</a></li>
        <li><a href="#services">Petit déménagement</a></li>
        <li><a href="#services">Urgences 24h/24</a></li>
      </ul>
    </div>
  </div>
  <div class="footer-bottom-layout">
    <div class="footer-copyright">© 2026 TouteSolution — Tous droits réservés.</div>
    <div class="footer-copyright"><a href="mentions-legales.html" style="color:inherit">Mentions légales</a> — <a href="cgv.html" style="color:inherit">Conditions Générales de Vente</a></div>
  </div>
</footer>

<script>
/* ==========================================
   MOBILE MENU TOGGLE
   ========================================== */
const navHamburger = document.getElementById('nav-hamburger');
const mobileMenu = document.getElementById('mobile-menu');

navHamburger.addEventListener('click', function() {
    const isOpen = mobileMenu.classList.toggle('open');
    navHamburger.classList.toggle('open', isOpen);
    navHamburger.setAttribute('aria-expanded', isOpen);
    document.body.style.overflow = isOpen ? 'hidden' : '';
});

mobileMenu.querySelectorAll('a').forEach(link => {
    link.addEventListener('click', function() {
        mobileMenu.classList.remove('open');
        navHamburger.classList.remove('open');
        navHamburger.setAttribute('aria-expanded', 'false');
        document.body.style.overflow = '';
    });
});

/* ==========================================
   ESTIMATOR CALCULATION ENGINE
   ========================================== */
// Grille tarifaire de base (estimation indicative marché parisien)
const tariffs = {
    moto2: 35,
    voiture: 55,
    camion12: 95,
    camion20: 160
};

// Zonage réel : 1 = Paris, 2 = petite couronne, 3 = grande couronne, 4 = hors IDF
const deptZone = { "75": 1, "92": 2, "93": 2, "94": 2, "77": 3, "78": 3, "91": 3, "95": 3, "other": 4 };

let currentUrgency = 'normal';

// Gestionnaire d'urgence interactif (Boutons radio style)
const urgencyButtons = document.querySelectorAll('#urgency-selector .urgency-btn');
urgencyButtons.forEach(button => {
    button.addEventListener('click', function() {
        urgencyButtons.forEach(btn => btn.classList.remove('active'));
        this.classList.add('active');
        currentUrgency = this.getAttribute('data-urgency');
    });
});

// Moteur de calcul au clic
document.getElementById('est-vehicle').addEventListener('change', function() {
    if (this.value) {
        document.getElementById('vehicle-error').classList.remove('visible');
        this.classList.remove('field-invalid');
    }
});

document.getElementById('btn-estimate').addEventListener('click', function() {
    const vehicleSelect = document.getElementById('est-vehicle');
    const vehicle = vehicleSelect.value;
    const pickup = document.getElementById('est-pickup').value;
    const delivery = document.getElementById('est-delivery').value;
    const vehicleError = document.getElementById('vehicle-error');

    // Validation d'input
    if (!vehicle) {
        vehicleError.classList.add('visible');
        vehicleSelect.classList.add('field-invalid');
        vehicleSelect.focus();
        return;
    }
    vehicleError.classList.remove('visible');
    vehicleSelect.classList.remove('field-invalid');

    // Base du calcul
    let calculatedPrice = tariffs[vehicle];

    // Majorations géographiques par zone réelle
    if (pickup !== delivery) {
        calculatedPrice += 20; // Majoration de transit inter-département

        const pickupZone = deptZone[pickup];
        const deliveryZone = deptZone[delivery];

        if (pickupZone === 4 || deliveryZone === 4) {
            calculatedPrice += 60; // Hors Île-de-France
        } else if (pickupZone === 3 || deliveryZone === 3) {
            calculatedPrice += 25; // Grande couronne
        }
    }

    // Majorations liées à l'urgence
    if (currentUrgency === 'urgent') {
        calculatedPrice *= 1.30; // +30%
    } else if (currentUrgency === 'super') {
        calculatedPrice *= 1.60; // +60%
    }

    // Arrondi de sécurité commercial propre
    const finalPrice = Math.round(calculatedPrice);

    // Rendu UI du résultat (format monétaire français)
    const resultBox = document.getElementById('estimate-result-box');
    const priceDisplay = document.getElementById('estimated-price');

    priceDisplay.textContent = finalPrice.toFixed(2).replace('.', ',') + " € HT";
    resultBox.style.display = 'block';
});

/* ==========================================
   FORM DISPATCHING (ENVOI RÉEL VIA FORMSUBMIT)
   ========================================== */
// FormSubmit relaie le formulaire par e-mail sans back-end.
// ⚠️ Première utilisation : FormSubmit envoie un e-mail de confirmation
// à Toutesolution.75@gmail.com qu'il faut valider une seule fois pour activer l'envoi.
const FORM_ENDPOINT = "https://formsubmit.co/ajax/Toutesolution.75@gmail.com";

const quoteForm = document.getElementById('quote-request-form');
const successBanner = document.getElementById('form-success-banner');
const errorBanner = document.getElementById('form-error-banner');
const submitButton = document.getElementById('btn-submit');

quoteForm.addEventListener('submit', function(event) {
    event.preventDefault();

    errorBanner.style.display = 'none';
    submitButton.disabled = true;
    submitButton.textContent = "Envoi en cours...";

    fetch(FORM_ENDPOINT, {
        method: 'POST',
        headers: { 'Accept': 'application/json' },
        body: new FormData(quoteForm)
    })
    .then(response => {
        if (!response.ok) throw new Error('Réponse serveur invalide');
        quoteForm.style.display = 'none';
        successBanner.style.display = 'block';
    })
    .catch(() => {
        errorBanner.style.display = 'block';
        submitButton.disabled = false;
        submitButton.textContent = "Envoyer ma demande";
    });
});
</script>
</body>
</html>
