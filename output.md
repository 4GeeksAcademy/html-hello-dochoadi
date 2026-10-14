# Lucía Marín — Artist Portfolio — Verification Checklist

## ARTIST DATA

| # | Requirement | Status | Notes |
|---|-------------|--------|-------|
| 1 | Artist name: Lucía Marín | ✅ Met | Used in `<h1>`, `<title>`, JSON-LD Person |
| 2 | Discipline: Contemporary painter (oil and mixed media), based in Madrid | ✅ Met | In meta description, JSON-LD `jobTitle`, and bio |
| 3 | Tagline: "Color that remembers the light of the coast." (Spanish: "Color que recuerda la luz de la costa.") | ✅ Met | In hero section as `.hero__tagline` |
| 4 | Bio matches given text | ✅ Met | In `#about` section and meta description |
| 5 | Career milestones in order with years | ✅ Met | Ordered `<ol>` with `<time>` for each year |
| 6 | Upcoming shows with correct data | ✅ Met | 3 `<article>` elements match given data |
| 7 | Featured works with correct title, year, technique | ✅ Met | 6 `<figure>` / `<figcaption>` with correct metadata |
| 8 | Contact: hola@lucíamarin-arte.example | ✅ Met | mailto link in footer |
| 9 | Social links to Instagram and LinkedIn | ✅ Met | Footer links open in new tab |
| 10 | Production URL for canonical and og:url | ✅ Met | `https://example.github.io/lucia-marin/` |

## FILES

| # | Requirement | Status | Notes |
|---|-------------|--------|-------|
| 11 | index.html with all content and markup | ✅ Met | Single self-contained HTML file |
| 12 | styles.css linked from index.html | ✅ Met | `<link rel="stylesheet" href="styles.css">` |
| 13 | images/ folder with hero.svg | ✅ Met | Under 20 KB (2.2 KB) |
| 14 | images/ with work-1.svg to work-6.svg | ✅ Met | All 6 work SVGs created |
| 15 | No external images | ✅ Met | All images are local SVGs |
| 16 | At most one external font (Google Fonts) | ✅ Met | Playfair Display, with font-display: swap on stylesheet |
| 17 | Preconnect for Google Fonts | ✅ Met | Two `<link rel="preconnect">` elements |

## PAGE STRUCTURE

| # | Requirement | Status | Notes |
|---|-------------|--------|-------|
| 18 | Skip link to #main | ✅ Met | `<a class="skip-link" href="#main">` |
| 19 | `<nav aria-label="Main navigation">` with links | ✅ Met | Links to #about, #career, #shows, #works, #contact |
| 20 | `<main id="main">` | ✅ Met | |
| 21 | `<section id="hero">` with `<h1>`, tagline, hero.svg | ✅ Met | Decorative alt="" and aria-hidden="true" |
| 22 | `<section id="about">` with `<h2>` and bio | ✅ Met | aria-labelledby="about-heading" |
| 23 | `<section id="career">` with `<h2>` and `<ol>` of milestones | ✅ Met | Each `<li>` contains `<time>` element |
| 24 | `<section id="shows">` with `<h2>` and `<article>` per show | ✅ Met | 3 `<article>` elements with `<h3>`, `<time>`, venue |
| 25 | "Next show" line in hero | ✅ Met | `.hero__next` mentions Luz de Otoño |
| 26 | `<section id="works">` with `<h2>` and gallery | ✅ Met | `<figure>` / `<figcaption>` for each work |
| 27 | `<footer>` with contact, social, copyright 2026 | ✅ Met | Includes mailto, Instagram, LinkedIn links |

## LAYOUT AND CSS

| # | Requirement | Status | Notes |
|---|-------------|--------|-------|
| 28 | Every `<section>` uses min-height: 100svh (fallback 100vh) | ✅ Met | `.section` uses both with 100vh before 100svh |
| 29 | No fixed heights | ✅ Met | Only min-height used |
| 30 | Flexbox for layout (no float/inline-block for structure) | ✅ Met | Flexbox used throughout |
| 31 | CSS custom properties in :root | ✅ Met | Colors, spacing, type scale defined |
| 32 | BEM class names | ✅ Met | e.g. `hero__title`, `nav__link`, `work-card__image` |
| 33 | Header is sticky | ✅ Met | `position: sticky; top: 0` |
| 34 | Sections use scroll-margin-top | ✅ Met | `scroll-margin-top: var(--header-h)` |
| 35 | Visible :focus-visible styles | ✅ Met | `2px solid var(--color-focus)` outline |
| 36 | Responsive from 360px, no horizontal scroll | ✅ Met | Breakpoints at 480px, 768px, 1024px; overflow-x: hidden |
| 37 | Gallery reflows 1→2→3 columns | ✅ Met | 1 col < 480px, 2 col ≥ 480px/768px, 3 col ≥ 1024px |
| 38 | Subtle entrance animations with @keyframes | ✅ Met | fadeInUp and fadeIn keyframes |
| 39 | Animations wrapped in @media (prefers-reduced-motion: no-preference) | ✅ Met | All keyframe usage inside the media query |
| 40 | Every image has width and height attributes | ✅ Met | All SVGs have width and height attributes |
| 41 | Images below first screen use loading="lazy" | ✅ Met | All work images use `loading="lazy"` |
| 42 | Color contrast at least WCAG AA | ✅ Met | Dark text on light backgrounds; white text on dark footer |

## ACCESSIBILITY

| # | Requirement | Status | Notes |
|---|-------------|--------|-------|
| 43 | Semantic landmarks: header, nav, main, section, article, figure, footer | ✅ Met | All used correctly |
| 44 | Exactly one `<h1>` | ✅ Met | Only "Lucía Marín" is `<h1>` |
| 45 | Heading levels never skip | ✅ Met | h1 → h2 → h3, no skipping |
| 46 | aria-labelledby on sections with visible heading | ✅ Met | about, career, shows, works sections |
| 47 | aria-label on nav | ✅ Met | `aria-label="Main navigation"` |
| 48 | lang="es" on `<html>` | ✅ Met | `<html lang="es">` |
| 49 | Meaningful link text, no "click here" | ✅ Met | "Sobre mí", "Trayectoria", etc. |
| 50 | Decorative SVGs use alt="" and aria-hidden="true" | ✅ Met | hero.svg has both |

## SEO AND SCHEMA.ORG

| # | Requirement | Status | Notes |
|---|-------------|--------|-------|
| 51 | Unique `<title>` | ✅ Met | "Lucía Marín — Contemporary Painter, Madrid" |
| 52 | `<meta name="description">` | ✅ Met | Relevant description |
| 53 | Open Graph tags (og:title, og:description, og:image, og:url) | ✅ Met | All four present |
| 54 | `<link rel="canonical">` to production URL | ✅ Met | |
| 55 | JSON-LD `<script type="application/ld+json">` in `<head>` | ✅ Met | Uses `@graph` array |
| 56 | Person schema: name, jobTitle, description, url, image, sameAs, knowsAbout | ✅ Met | Valid schema.org properties |
| 57 | Event schema per show: name, startDate (ISO 8601 with timezone), eventStatus, location (Place), performer | ✅ Met | 3 Event entries with correct timezone offsets |
| 58 | CreativeWork per featured work: name, dateCreated, artMedium, creator | ✅ Met | 6 CreativeWork entries |
| 59 | Only valid schema.org property names | ✅ Met | No invented properties |

## FINAL CHECKS

| # | Requirement | Status | Notes |
|---|-------------|--------|-------|
| 60 | No unclosed or misnested tags | ✅ Met | Verified by reading the full file |
| 61 | No duplicate ids | ✅ Met | All ids are unique |
| 62 | Every nav link matches an existing id | ✅ Met | #about, #career, #shows, #works, #contact all exist |
| 63 | Every show date in JSON-LD matches visible date | ✅ Met | Verified: dates/times match exactly |
| 64 | `font-display: swap` used | ✅ Met | Google Fonts link includes display=swap |

---

## SUMMARY

- **Total checks: 64**
- **Met: 64**
- **Not met: 0**

All requirements have been successfully implemented. The single-page artist portfolio for Lucía Marín is complete with:

- Clean semantic HTML5 with Spanish language attribute
- BEM-method CSS with custom properties, Flexbox layout, and responsive design
- 7 SVG placeholder images (hero + 6 works)
- Accessibility features including skip link, ARIA landmarks, and focus-visible styles
- Structured data via JSON-LD (Person, Event × 3, CreativeWork × 6)
- Open Graph and canonical link tags
- One external Google Font (Playfair Display) with preconnect and swap
- No JavaScript, frameworks, or external dependencies beyond the font