# 🎨 Lucía Marín — Artist Portfolio

A single-page portfolio website for **Lucía Marín**, a fictional contemporary painter based in Madrid who works in oil and mixed media. The site is written in plain **HTML5 and CSS3**. It has no JavaScript, framework or build step, and it puts semantic markup, accessibility and SEO first.

> *"Color que recuerda la luz de la costa."*: color that remembers the light of the coast.

**Author:** [@dochoadi](https://github.com/dochoadi)

---

## ✨ Features

- **Semantic HTML5**: `header`, `nav`, `main`, `section`, `article`, `figure` and `footer` landmarks, with exactly one `<h1>` and no skipped heading levels.
- **Accessible**:
  - skip link and `aria-labelledby` on every section
  - visible `:focus-visible` styles
  - WCAG AA color contrast
  - animations only when the user hasn't asked for reduced motion (`prefers-reduced-motion`)
- **Responsive**: works from 360px wide upward. The gallery goes from 1 to 2 to 3 columns, with no horizontal scroll.
- **Modern CSS**:
  - BEM naming
  - design tokens as custom properties
  - Flexbox layout
  - sticky header
  - `100svh` sections
  - `@keyframes` entrance animations
- **SEO ready**: meta description, Open Graph tags and a canonical URL.
- **Structured data**: a JSON-LD `@graph` with one `Person`, three `Event`s and six `CreativeWork`s, all using valid schema.org properties.
- **Lightweight**: local SVG images with `width` and `height` set and `loading="lazy"`, plus a single Google Font (Playfair Display) loaded with `preconnect` and `display=swap`.

## 🗂️ Page Sections

| Section | Content |
|---------|---------|
| **Hero** | Artist name, tagline, and the next upcoming show |
| **Sobre mí** | Short biography |
| **Trayectoria** | Career milestones from 2017 to 2025 |
| **Exposiciones** | Upcoming shows in Madrid, Málaga and Bilbao |
| **Obras** | Gallery of six selected works with year and technique |
| **Contacto** | Email, Instagram and LinkedIn |

## 📁 Project Structure

```
├── index.html      # Markup, meta tags and JSON-LD structured data
├── styles.css      # All styles (BEM + custom properties)
├── images/         # hero.svg + work-1.svg … work-6.svg
├── context.md      # Project context and requirements
├── output.md       # Requirements verification checklist
└── server.py       # Local Flask dev server
```

## 🚀 Run Locally

```bash
pip3 install flask && python3 server.py
```

Then open <http://localhost:3000>.

## 🛠️ Built With

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![Schema.org](https://img.shields.io/badge/Schema.org-JSON--LD-blue)

## 🙏 Credits

Built as part of the [4Geeks Academy](https://4geeksacademy.com) Full Stack Developer course, starting from the [html-hello](https://github.com/4GeeksAcademy/html-hello) template. Lucía Marín and all the content on the site are fictional.
