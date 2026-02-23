# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static personal resume/portfolio website hosted on GitHub Pages at `maxcelos.github.io`. Modern single-page site with dark/light mode, built with Tailwind CSS (Play CDN), Lucide icons, and vanilla JavaScript — no build step required.

## Deployment

Push to `master` branch to deploy via GitHub Pages. There is no build step — the site is served as static files directly.

## Architecture

- **`index.html`** — The entire site is a single HTML file containing all HTML, inline Tailwind config, custom CSS, and JavaScript. Sections: Hero, About, Experience, Skills, Projects, Education, Testimonial, Contact/Footer.
- **`assets/images/`** — Profile photo (`marcelo.jpg`, `profile.jpg`) and language flag icons (`Brazil.png`, `Spain.png`, `United-States.png`)
- **`favicon.ico`** — Site favicon

## Tech Stack

- **Tailwind CSS** via Play CDN (`cdn.tailwindcss.com`) — configured inline in `<script>` with custom colors and fonts, `darkMode: 'class'`
- **Google Fonts** — Inter (weights 300–700)
- **Lucide Icons** via CDN (`unpkg.com/lucide@latest`) — lightweight SVG icon set, initialized with `lucide.createIcons()`
- **Vanilla JavaScript** — no jQuery, no framework dependencies

## Key Details

- No package manager, build tool, or test framework is configured
- Dark/light mode toggle persists to `localStorage` (key: `theme`, values: `dark`/`light`); defaults to dark
- Scroll animations use Intersection Observer with `.fade-up` / `.visible` CSS classes
- Active nav link highlighting uses a separate Intersection Observer
- All styles are either Tailwind utility classes or defined in the inline `<style>` block
- Language is set to `en` (English) in the HTML lang attribute
- Color scheme: dark slate (`#0f172a` / `slate-950`) + cyan accent (`#06b6d4` / `brand`)
