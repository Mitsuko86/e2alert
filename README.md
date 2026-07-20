/* ===========================================================
   E2ALERT — styles
   Font pairing: Space Grotesk (display) + Inter (body/UI)
   =========================================================== */

@import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@500;600;700&family=Inter:wght@400;500;600;700&display=swap');

:root {
  /* Color tokens */
  --blue-600: #345CEF;
  --blue-700: #2846C4;
  --blue-500: #5578F5;
  --blue-100: #E7ECFE;
  --blue-50:  #F4F6FE;
  --navy-900: #0D1230;
  --navy-800: #12173A;
  --green-600: #17A363;
  --ink-900: #10142A;
  --ink-600: #4B5170;
  --ink-400: #848AA6;
  --white: #FFFFFF;
  --line: #E4E7F5;

  --font-display: 'Space Grotesk', 'Segoe UI', sans-serif;
  --font-body: 'Inter', 'Segoe UI', sans-serif;

  --radius-md: 12px;
  --radius-lg: 20px;
  --radius-full: 999px;

  --shadow-card: 0 1px 2px rgba(16, 20, 42, 0.04), 0 8px 24px rgba(16, 20, 42, 0.06);
  --shadow-lift: 0 12px 32px rgba(52, 92, 239, 0.18);

  --container: 1160px;
}

* { box-sizing: border-box; }

html {
  scroll-behavior: smooth;
}

@media (prefers-reduced-motion: reduce) {
  html { scroll-behavior: auto; }
  * { animation-duration: 0.001ms !important; animation-iteration-count: 1 !important; transition-duration: 0.001ms !important; }
}

body {
  margin: 0;
  font-family: var(--font-body);
  color: var(--ink-900);
  background: var(--white);
  -webkit-font-smoothing: antialiased;
  line-height: 1.55;
}

h1, h2, h3, h4 {
  font-family: var(--font-display);
  color: var(--navy-900);
  margin: 0;
  line-height: 1.15;
  letter-spacing: -0.01em;
}

p { margin: 0; }

a { color: inherit; text-decoration: none; }

img { max-width: 100%; display: block; }

.container {
  width: 100%;
  max-width: var(--container);
  margin: 0 auto;
  padding: 0 24px;
}

:focus-visible {
  outline: 3px solid var(--blue-500);
  outline-offset: 2px;
  border-radius: 4px;
}

.skip-link {
  position: absolute;
  left: -9999px;
  top: 0;
  background: var(--blue-600);
  color: var(--white);
  padding: 12px 18px;
  border-radius: 0 0 8px 0;
  z-index: 100;
  font-weight: 600;
  font-size: 0.9rem;
}

.skip-link:focus {
  left: 0;
}

/* ---------- Buttons ---------- */

.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  padding: 13px 26px;
  border-radius: var(--radius-full);
  font-family: var(--font-body);
  font-weight: 600;
  font-size: 0.95rem;
  border: none;
  cursor: pointer;
  transition: transform 0.15s ease, box-shadow 0.15s ease, background-color 0.15s ease;
  white-space: nowrap;
}

.btn:active { transform: translateY(1px); }

.btn-primary {
  background: var(--blue-600);
  color: var(--white);
  box-shadow: var(--shadow-lift);
}

.btn-primary:hover {
  background: var(--blue-700);
  box-shadow: 0 14px 34px rgba(52, 92, 239, 0.26);
}

.btn-light {
  background: var(--white);
  color: var(--blue-700);
}

.btn-light:hover {
  background: var(--blue-50);
}

.btn-block { width: 100%; }

/* ---------- Header ---------- */

.site-header {
  position: sticky;
  top: 0;
  z-index: 50;
  background: rgba(255, 255, 255, 0.9);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--line);
}

.site-header .container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 76px;
}

.logo img { height: 26px; width: auto; }

.main-nav {
  display: flex;
  align-items: center;
  gap: 40px;
}

.main-nav a {
  font-size: 0.95rem;
  font-weight: 500;
  color: var(--ink-600);
  transition: color 0.15s ease;
}

.main-nav a:hover { color: var(--blue-600); }

.header-actions { display: flex; align-items: center; gap: 24px; }

.nav-toggle {
  display: none;
  background: none;
  border: none;
  padding: 6px;
  cursor: pointer;
}

.nav-toggle span {
  display: block;
  width: 22px;
  height: 2px;
  background: var(--navy-900);
  margin: 5px 0;
  transition: transform 0.2s ease, opacity 0.2s ease;
}

/* ---------- Hero ---------- */

.hero {
  background: linear-gradient(180deg, var(--blue-50) 0%, #FFFFFF 100%);
  padding: 88px 0 96px;
  overflow: hidden;
}

.hero .container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 64px;
  align-items: center;
}

.eyebrow {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: var(--blue-100);
  color: var(--blue-700);
  font-size: 0.8rem;
  font-weight: 600;
  padding: 6px 14px;
  border-radius: var(--radius-full);
  margin-bottom: 20px;
  letter-spacing: 0.01em;
}

.eyebrow .dot {
  width: 7px;
  height: 7px;
  border-radius: 50%;
  background: var(--green-600);
  box-shadow: 0 0 0 3px rgba(23, 163, 99, 0.18);
}

.hero h1 {
  font-size: clamp(2.1rem, 4vw, 3.1rem);
  font-weight: 700;
  margin-bottom: 18px;
}

.hero h1 .accent { color: var(--blue-600); }

.hero-sub {
  font-size: 1.1rem;
  font-weight: 600;
  color: var(--ink-900);
  margin-bottom: 14px;
}

.hero-copy {
  font-size: 1.02rem;
  color: var(--ink-600);
  max-width: 46ch;
  margin-bottom: 32px;
}

.hero-cta-row {
  display: flex;
  align-items: center;
  gap: 20px;
  flex-wrap: wrap;
}

.hero-note {
  font-size: 0.85rem;
  color: var(--ink-400);
}

.affiliate-disclaimer {
  font-size: 0.78rem;
  line-height: 1.5;
  color: var(--ink-400);
  max-width: 52ch;
  margin-top: 16px;
}

.discord-cta .affiliate-disclaimer {
  margin: 18px auto 0;
}

.affiliate-disclaimer-dark {
  color: rgba(255, 255, 255, 0.65);
  max-width: 56ch;
  margin: 18px auto 0;
}

.hero-visual {
  position: relative;
}

.hero-visual .photo-frame {
  border-radius: var(--radius-lg);
  overflow: hidden;
  box-shadow: var(--shadow-card);
  border: 1px solid var(--line);
}

.hero-visual img { width: 100%; height: auto; }

.floating-chip {
  position: absolute;
  background: var(--white);
  border-radius: var(--radius-md);
  box-shadow: var(--shadow-card);
  padding: 12px 16px;
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: 0.85rem;
  font-weight: 600;
  border: 1px solid var(--line);
}

.floating-chip.chip-top {
  top: -18px;
  right: 24px;
}

.floating-chip.chip-bottom {
  bottom: -20px;
  left: -18px;
}

.floating-chip .chip-icon {
  width: 30px;
  height: 30px;
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1rem;
  flex-shrink: 0;
}

.chip-top .chip-icon { background: var(--blue-100); }
.chip-bottom .chip-icon { background: #DFF6EA; }

.chip-label-sub { display: block; font-weight: 400; color: var(--ink-400); font-size: 0.72rem; margin-top: 1px; }

/* ---------- Feature grid ---------- */

.feature-grid-section {
  padding: 0 0 96px;
}

.feature-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 20px;
  margin-top: -56px;
  position: relative;
  z-index: 2;
}

.feature-card {
  background: var(--white);
  border: 1px solid var(--line);
  border-radius: var(--radius-lg);
  padding: 28px 22px;
  box-shadow: var(--shadow-card);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.feature-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 16px 36px rgba(16, 20, 42, 0.09);
}

.feature-icon {
  width: 46px;
  height: 46px;
  border-radius: 12px;
  background: var(--blue-100);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.3rem;
  margin-bottom: 18px;
}

.feature-card h3 {
  font-size: 1.05rem;
  font-weight: 600;
  margin-bottom: 8px;
}

.feature-card p {
  color: var(--ink-600);
  font-size: 0.92rem;
}

/* ---------- Section headers ---------- */

.section-head {
  text-align: center;
  max-width: 620px;
  margin: 0 auto 56px;
}

.section-head .kicker {
  display: block;
  font-size: 0.8rem;
  font-weight: 700;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--blue-600);
  margin-bottom: 12px;
}

.section-head h2 {
  font-size: clamp(1.7rem, 3vw, 2.3rem);
  margin-bottom: 14px;
}

.section-head p {
  color: var(--ink-600);
  font-size: 1.02rem;
}

/* ---------- How it works ---------- */

.how-it-works {
  background: var(--blue-50);
  padding: 96px 0;
}

.steps {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
  counter-reset: step;
  margin-bottom: 64px;
}

.step-card {
  background: var(--white);
  border-radius: var(--radius-lg);
  border: 1px solid var(--line);
  padding: 32px 26px;
  position: relative;
}

.step-card .step-number {
  font-family: var(--font-display);
  font-size: 0.8rem;
  font-weight: 700;
  color: var(--blue-500);
  letter-spacing: 0.06em;
  margin-bottom: 18px;
  display: block;
}

.step-icon {
  width: 48px;
  height: 48px;
  border-radius: 12px;
  background: var(--blue-100);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.4rem;
  margin-bottom: 18px;
}

.step-card h3 {
  font-size: 1.08rem;
  font-weight: 600;
  margin-bottom: 8px;
}

.step-card p {
  color: var(--ink-600);
  font-size: 0.92rem;
}

.step-connector {
  display: none;
}

.discord-cta {
  background: var(--white);
  border-radius: var(--radius-lg);
  border: 1px solid var(--line);
  padding: 56px 40px;
  text-align: center;
  max-width: 760px;
  margin: 0 auto;
}

.discord-cta h3 {
  font-size: 1.5rem;
  margin-bottom: 14px;
}

.discord-cta p {
  color: var(--ink-600);
  max-width: 48ch;
  margin: 0 auto 28px;
}

/* ---------- FAQ ---------- */

.faq-section {
  padding: 100px 0;
}

.faq-layout {
  display: grid;
  grid-template-columns: 0.85fr 1.15fr;
  gap: 56px;
  align-items: start;
}

.faq-visual {
  position: sticky;
  top: 110px;
  text-align: center;
}

.faq-visual img {
  width: 100%;
  max-width: 380px;
  margin: 0 auto;
}

.faq-list {
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.faq-item {
  border: 1px solid var(--line);
  border-radius: var(--radius-md);
  background: var(--white);
  overflow: hidden;
}

.faq-item[open] {
  border-color: var(--blue-500);
  box-shadow: 0 4px 18px rgba(52, 92, 239, 0.08);
}

.faq-item summary {
  list-style: none;
  cursor: pointer;
  padding: 20px 22px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 16px;
  font-weight: 600;
  font-size: 1rem;
  color: var(--navy-900);
}

.faq-item summary::-webkit-details-marker { display: none; }

.faq-toggle-icon {
  flex-shrink: 0;
  width: 28px;
  height: 28px;
  border-radius: 50%;
  background: var(--blue-50);
  color: var(--blue-600);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.1rem;
  transition: transform 0.2s ease, background-color 0.2s ease;
}

.faq-item[open] .faq-toggle-icon {
  background: var(--blue-600);
  color: var(--white);
  transform: rotate(45deg);
}

.faq-answer {
  padding: 0 22px 22px;
  color: var(--ink-600);
  font-size: 0.95rem;
  max-width: 62ch;
}

/* ---------- Final CTA banner ---------- */

.final-cta {
  background: linear-gradient(135deg, var(--blue-600) 0%, var(--navy-900) 130%);
  padding: 72px 0;
  text-align: center;
}

.final-cta h2 {
  color: var(--white);
  font-size: clamp(1.6rem, 3vw, 2.2rem);
  margin-bottom: 14px;
}

.final-cta p {
  color: rgba(255, 255, 255, 0.82);
  margin-bottom: 32px;
  font-size: 1.05rem;
}

/* ---------- Footer ---------- */

.site-footer {
  background: var(--navy-900);
  padding: 40px 0;
}

.site-footer .container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 16px;
}

.site-footer .logo img { height: 22px; }

.footer-copy {
  color: rgba(255, 255, 255, 0.5);
  font-size: 0.85rem;
}

.footer-links {
  display: flex;
  gap: 24px;
}

.footer-links a {
  color: rgba(255, 255, 255, 0.65);
  font-size: 0.85rem;
  transition: color 0.15s ease;
}

.footer-links a:hover { color: var(--white); }

/* ---------- Responsive ---------- */

@media (max-width: 980px) {
  .hero .container { grid-template-columns: 1fr; }
  .hero-visual { order: -1; max-width: 480px; margin: 0 auto; }
  .feature-grid { grid-template-columns: repeat(2, 1fr); margin-top: 40px; }
  .steps { grid-template-columns: 1fr; }
  .faq-layout { grid-template-columns: 1fr; }
  .faq-visual { position: static; margin-bottom: 8px; }
  .faq-visual img { max-width: 260px; }
}

@media (max-width: 720px) {
  .main-nav { display: none; }
  .nav-toggle { display: block; }
  .header-actions .btn-primary { display: none; }

  body.nav-open .main-nav {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 4px;
    position: absolute;
    top: 76px;
    left: 0;
    right: 0;
    background: var(--white);
    border-bottom: 1px solid var(--line);
    padding: 16px 24px 24px;
  }

  body.nav-open .main-nav a { padding: 10px 0; width: 100%; }
  body.nav-open .header-actions .btn-primary { display: none; }

  .hero { padding: 48px 0 72px; }
  .feature-grid { grid-template-columns: 1fr; margin-top: 32px; }
  .floating-chip { display: none; }
  .discord-cta { padding: 40px 22px; }
  .site-footer .container { flex-direction: column; text-align: center; }
}
