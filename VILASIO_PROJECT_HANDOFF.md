# VILASIO — Project Handoff Document
## Ultimo aggiornamento: Aprile 2026

---

## CHI SIAMO
VILASIO è una piattaforma di Financial Analytics & Market Research. Sito statico su GitHub Pages (repo: `gdurante1705/vilasio`), backend Python/Flask su Render.
- **URL:** vilasio.com (Cloudflare)
- **Backend:** https://vilasio-cot-backend.onrender.com
- **Email:** info@vilasio.com
- **"VILASIO" sempre MAIUSCOLO nel testo**

---

## STACK TECNICO
- Frontend: HTML statici su GitHub Pages (no framework, no build system)
- Backend: Python/Flask su Render free tier
- Librerie: Chart.js 4.4.1, D3 v7, Three.js r128
- Font: DM Sans (heading) + IBM Plex Sans (body) + IBM Plex Mono (labels/mono)
- Google Fonts link: `family=DM+Sans:wght@300;400;500;600;700&family=IBM+Plex+Sans:wght@300;400;500;600&family=IBM+Plex+Mono:wght@400;500`

---

## DESIGN SYSTEM

### Palette Light Mode (default)
- Background: #FAFAF8 (crema)
- Background secondario: #F2F1ED
- Card/chart sfondo: #F5F4F1
- Bianco: #FFFFFF
- Testo principale: #111111 / #222222
- Testo secondario: #555555 / #6B6B6B
- Bordi: #D8D8D4 / #E8E6E1
- Accento oro: #C5A33C (SOLO per accenti, overline, emphasis — MAI per UI)

### Palette Dark Mode
- Background: #111118
- Card/panel: #1a1a22
- Testo: #e0e0e0 / #f0f0f0
- Bordi: rgba(255,255,255,0.08)
- Oro: #C5A33C (invariato)

### Font
- Titoli/heading: DM Sans, weight 500-700
- Body: IBM Plex Sans, weight 300-500
- Labels/mono: IBM Plex Mono, weight 400-500
- CSS vars: `--heading`, `--body`, `--mono`

### Regole Design (NON dimenticare MAI)
- HOW TO READ sotto ogni chart (tool pages)
- `tension:0` su tutti i chart line
- `beginAtZero:false` dove la scala a zero è inutile
- Colori dati SOLO per dati, mai per UI
- © 2026 VILASIO. Financial Analytics & Market Research.
- Dark mode toggle con localStorage su tutte le pagine

---

## STRUTTURA SITO — 17 PAGINE

### Site Pages (nav: COT Intelligence · Insights · Methodology · [The Owl CTA])
| File | Descrizione | Stato |
|------|-------------|-------|
| index.html | Landing page — hero video full-width stile Citadel, headline "The edge belongs to those who look deeper." | ✅ Completo |
| about.html | Methodology page — "How We Read Markets", framework analitico, data sources | ✅ Completo |
| owl.html | The Owl — pagina premium, layout 3 colonne dashboard (card sx + hero centro + card dx + geopolitical sotto) | ✅ Completo |
| blog.html | Insights — link ad articoli LinkedIn del fondatore | ✅ Completo |
| contact.html | Pagina contatti con form | ✅ Completo |
| privacy.html | Privacy Policy — GDPR compliant | ✅ Completo |
| terms.html | Terms of Use — 14 sezioni | ✅ Completo |
| cookie.html | Cookie Policy | ✅ Completo |

### Tool Pages (nav: The Owl + 7 tool links + Geopolitical)
| File | Descrizione | Stato |
|------|-------------|-------|
| cot.html | COT Intelligence — CFTC data, 39 futures, heatmap, Z-Score, Capital Flow, Sankey | ✅ Completo (GRATUITO) |
| macro.html | Macro Dashboard — regime quadrant, inflation, labor, banking health | ✅ Completo (PREMIUM) |
| bonds.html | Bonds & Rates — Treasury yields, credit spreads, MOVE Index | ✅ Completo (PREMIUM) |
| liquidity.html | Liquidity Monitor — Fed balance sheet, RRP, TGA, SOFR | ✅ Completo (PREMIUM) |
| crossmarket.html | Cross-Market — sector rotation, currency strength, commodities | ✅ Completo (PREMIUM) |
| earnings.html | Earnings Intelligence — PEAD scanner, EPS history, drift | ✅ Completo (PREMIUM) |
| congressional.html | Congressional — insider trading, SEC Form 4 | ✅ Completo (PREMIUM) |
| geopolitical.html | Geopolitical Risk — AI-GPR index, D3 globe, 120+ countries | ✅ Completo (PREMIUM) |

### Navigazione
- **Site pages nav:** COT Intelligence → cot.html | Insights → blog.html | Methodology → about.html | [CTA] The Owl → owl.html
- **Tool pages nav:** The Owl → owl.html | Liquidity | Bonds | Macro | Cross-Market | Earnings | Congressional | Geopolitical
- **Footer (tutte):** Privacy Policy | Terms of Use | Cookie Policy | Contact
- **Disclaimer (tutte):** 4 paragrafi standard sotto il footer

---

## COSA È STATO COMPLETATO

### Landing Page (index.html)
- Hero video full-width stile Citadel (3 clip stock montati con ffmpeg, 32s seamless loop)
- Headline: "The edge belongs to those who look deeper." ("look deeper." in oro)
- Testo bianco sovrapposto sul video con overlay gradiente da sx (scuro) a dx (trasparente)
- Nav Citadel full-width: logo sx, link centro, "The Owl" CTA dx
- Sezioni: What We Track (6 card), Stats Strip, Methodology (2 paragrafi), Platform (2 card: COT + The Owl), Footer, Disclaimer

### Methodology Page (about.html)
- Titolo: "How We Read Markets"
- Sezioni: Our Approach, Analytical Framework (prosa, no card numerate), Data Sources (CFTC, Fed, Treasury, BLS, CBOE, SEC, ICE/CME, FRED), What We Are Not, Built by Traders
- Tono BlackRock istituzionale

### Light Theme + Dark Mode
- Tutte 17 pagine convertite al light theme (#FAFAF8 crema)
- Dark mode toggle (icona luna/sole) su tutte le pagine con localStorage
- Grigi scuriti (#222/#555) per leggibilità
- Card/chart con sfondo #F5F4F1
- Geopolitical globe: sfondo #020408 in dark mode per fondersi con star field
- COT Sankey/flow bars: label dinamiche con _txtColor()/_subColor()

### Coerenza Visiva (audit completato)
- Font identici su tutte 17 pagine (DM Sans + IBM Plex Sans + IBM Plex Mono)
- Logo SVG base64 con filter:brightness(0) in light, filter:none in dark
- Nav pixel-identical su tutte le pagine dello stesso gruppo
- Footer identico ovunque (4 link + copyright)
- Disclaimer 4 paragrafi ovunque

### Performance
- 10MB file orfani rimossi (layers-closed.png, layers-open.png, logo.jpg, logo.png, noBgBlack.png, noBgWhite.png)
- Favicon (icon.ico) e Social_Profile.jpg aggiunti al repo
- Video hero: 7MB, preload="metadata"
- theme-color meta tag su tutte le pagine
- Alt text su tutti i logo

### Mobile Responsive
- Breakpoint 960px e 768px su tutte le pagine
- Geopolitical globe: 3col→1col a 960px
- Macro regime sidebar: collassa a 960px
- Liquidity stats: breakpoint 768px aggiunto
- Table overflow-x:auto su crossmarket/earnings

### COT Data Freshness Fix (Aprile 2026)
- **Problema risolto:** dati COT stale per-market dopo release CFTC del venerdì. Utenti vedevano header con reportDate corretto ma singoli mercati con date diverse (es. OJ 2026-03-24, Copper 2026-03-31 mentre header diceva 2026-04-14)
- **Root cause:** localStorage frontend (prefisso `vcot2_`) cachava per-market con scadenza "sabato UTC prossimo", servendo dati stale anche dopo release CFTC
- **Fix applicato:**
  - Backend: `CACHE_TTL_COT` ridotto da 86400s (24h) a 3600s (1h) per freshness post-release CFTC
  - Backend: aggiunto campo top-level `latestReportDate` in `/api/cot/summary`
  - Frontend: bump cache prefix `vcot2_` → `vcot3_` (invalidazione forzata cache esistente utenti)
  - Frontend: `lS()` salva anche `reportDate` nella entry localStorage
  - Frontend: `lG(key, expectedRd)` invalida cache se reportDate cachato diverge da `LATEST_REPORT_DATE` del summary
  - Frontend: variabile globale `LATEST_REPORT_DATE` popolata da `rHM()` prima che `lD()` venga chiamata
- **Commit:** backend `0b9bf1e`, frontend `643253a`

---

## COSA MANCA — PROSSIMI STEP (in ordine di priorità)

### 1. Dark Mode Chart Fix (6 tool pages)
**Priorità: ALTA — bug visivo**
Le pagine liquidity, bonds, macro, crossmarket, earnings, congressional hanno ancora tooltip e griglia dei chart hardcoded in bianco quando si attiva il dark mode. Stesso problema che è stato fixato su geopolitical e cot. Serve applicare lo stesso pattern: colori dinamici basati su `_isDark()` o `html[data-theme="dark"]` per assi, gridline, tooltip background/text.

### 2. SEO
**Priorità: MEDIA**
- Creare sitemap.xml con tutte le 17 pagine
- Creare robots.txt
- Aggiungere structured data (Organization, WebSite)
- Canonical URLs su tutte le pagine
- Verificare meta description su tutte le pagine

### 3. Monetizzazione
**Priorità: ALTA — revenue**
- Supabase Auth per autenticazione utenti
- Stripe Integration per pagamenti
- Paywall: COT Intelligence resta GRATUITO, i 7 tool premium (The Owl) richiedono abbonamento
- Pricing page su owl.html (o pagina dedicata)
- Email onboarding flow
- Logica: utente non autenticato che visita una tool page premium → redirect a owl.html con prompt di login/signup

### 4. Blog con Contenuto Proprio
**Priorità: BASSA**
- Articoli interni sul sito invece che link a LinkedIn
- Sistema semplice (HTML statico o markdown → HTML)
- Categorie: Market Analysis, Tool Updates, Methodology

---

## BACKEND — Stato Tecnico

### API Endpoints
- `/api/cot/{market_code}?weeks={N}` — dati COT per mercato
- `/api/cot/summary` — sommario tutti i mercati + campo top-level `latestReportDate` (usato dal frontend per cache invalidation)
- `/api/cot/flow` — capital flow data
- `/api/macro` — dati macro
- `/api/bonds` — dati bonds/rates
- `/api/liquidity` — dati liquidità
- `/api/crossmarket` — dati cross-market
- `/api/earnings` — dati earnings/PEAD
- `/api/congressional` — dati congressional trading
- `/api/geopolitical` — dati geopolitical risk

### Infrastruttura
- Cache aggressiva su tutti gli endpoint (TTL ottimizzati)
- Batch download yfinance in chunk da 8 (anti-OOM)
- PEAD background loop ogni 6h
- UptimeRobot: 9 monitor attivi (keep-alive + performance)
- Skeleton loaders su tutte le pagine tool

### UptimeRobot Monitor
1. `/health` — 5 min
2. `/api/crossmarket` — 5 min
3. `/api/macro` — 5 min
4. `/api/congressional` — 5 min
5. `/api/bonds` — 5 min
6. `/api/liquidity` — 5 min
7. `/api/cot/summary` — 5 min
8. `/api/geopolitical` — 5 min
9. `/api/earnings` — 20 min

---

## REGOLE IMPORTANTI PER CLAUDE CODE

### NON fare mai:
- NON usare font diversi da DM Sans / IBM Plex Sans / IBM Plex Mono
- NON usare colori fuori dalla palette (no blu, viola, rosa random)
- NON mostrare i 7 tool premium nella nav delle site pages
- NON rimuovere HOW TO READ dai chart
- NON mettere tension diversa da 0 sui chart line
- NON menzionare NQ, ATAS, dxFeed, Rithmic, prop firms, Level 2, footprint, tape reading, scalping
- NON rompere il dark mode toggle esistente
- NON rimuovere la cache invalidation by reportDate in cot.html (`LATEST_REPORT_DATE` + `lG(key, expectedRd)`) — è il fix che previene dati COT stale post-CFTC release
- NON cambiare il prefisso cache frontend (`vcot3_`) senza aver valutato l'impatto sugli utenti esistenti (cambiandolo si invalida tutta la cache degli utenti attivi)
- NON cambiare la struttura nav senza chiedere

### Fare sempre:
- Testare sia light che dark mode dopo ogni modifica
- Pushare su GitHub dopo ogni gruppo di fix
- Mantenere coerenza con le altre pagine (confrontare prima di modificare)
- Usare le CSS variables (--heading, --body, --mono, --bg, --ink, --gold, etc.)
- Verificare che il logo sia visibile in entrambi i temi
