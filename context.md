# Project Context — Lucía Marín Artist Portfolio

## Overview

A single-page portfolio website for **Lucía Marín**, a contemporary painter based in Madrid who works in oil and mixed media. The page content is in Spanish (`lang="es"`). The project was built from the 4Geeks Academy `html-hello` template.

- **Tagline:** "Color que recuerda la luz de la costa."
- **Production URL (canonical / og:url):** `https://example.github.io/lucia-marin/`
- **Contact:** hola@lucíamarin-arte.example · Instagram · LinkedIn

## Tech Stack

- Plain HTML5 + CSS3. There is no JavaScript, framework or build step.
- One external font: Google Fonts **Playfair Display** (with `preconnect` and `display=swap`).
- All images are local SVGs.
- Local dev server: `server.py` (Flask) on port 3000. Install and run it with `pip3 install flask && python3 server.py`.

## File Structure

| Path | Purpose |
|------|---------|
| `index.html` | All markup, meta tags, Open Graph and JSON-LD structured data |
| `styles.css` | All styles: BEM classes, custom properties in `:root`, Flexbox layout, animations, breakpoints |
| `images/hero.svg` | Decorative hero background (`alt=""`, `aria-hidden="true"`) |
| `images/work-1.svg` … `work-6.svg` | Placeholder artwork for the gallery (lazy-loaded) |
| `output.md` | Verification checklist: 64 requirements, all marked as met |
| `server.py` | Flask static server for local preview |
| `context.md` | This file |

## Page Sections

1. **Skip link**, which jumps to `#main`
2. **Header**: a sticky `<nav aria-label="Main navigation">` that links to every section
3. **Hero** (`#hero`): `<h1>`, tagline, next-show line and hero image
4. **About** (`#about`): biography
5. **Career** (`#career`): `<ol>` of milestones with `<time>` (2017, 2019, 2021, 2023, 2025)
6. **Shows** (`#shows`): three `<article>` cards
   - *Luz de Otoño*: Sala Ámbar, Madrid. 7 Nov – 15 Dec 2026, opening at 19:00
   - *Mareas Interiores*: Galería Faro, Málaga. 12 Feb 2027, opening at 20:00
   - *Cuaderno de Viaje*: Centro Cultural Norte, Bilbao. 20 May 2027, opening at 18:30
7. **Works** (`#works`): six `<figure>` cards (1 → 2 → 3 columns)
   - Puerto al Amanecer (2024), Habitación con Mar (2023), Sal Sobre Papel (2022),
     Memoria de la Costa (2025), Ventana Sur (2021), Marea Baja (2024)
8. **Footer** (`#contact`): email, social links and © 2026

## Requirements & Conventions

- **Layout:** Flexbox only. Each section has `min-height: 100vh` and then `100svh`. No fixed heights. Sections set `scroll-margin-top` so the sticky header does not cover them.
- **CSS:** BEM naming and design tokens (colors, spacing, type scale) as custom properties.
- **Responsive:** must work from 360px wide with no horizontal scroll. Breakpoints are at 480, 768 and 1024px.
- **Animations:** `@keyframes` fadeIn and fadeInUp, used only inside `@media (prefers-reduced-motion: no-preference)`.
- **Accessibility:** semantic landmarks, exactly one `<h1>`, no skipped heading levels, `aria-labelledby` on sections, visible `:focus-visible` outline, WCAG AA contrast.
- **Images:** every `<img>` has `width` and `height`. Images below the first screen use `loading="lazy"`.
- **SEO:** unique `<title>`, meta description, Open Graph tags and canonical link.
- **Structured data:** JSON-LD `@graph` with one Person, three Events (ISO 8601 dates with timezone) and six CreativeWorks. Only valid schema.org properties are allowed.
- **Performance target:** PageSpeed Insights score of **≥ 80**.

## Status

- All 64 checklist items in `output.md` are marked as met.
- **Open issue:** PageSpeed Performance scored **61**, below the required 80.
