# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal profile/portfolio site for Jason Yang (BizOps Lead at D.CAMP). This is a static single-page site with no build system, bundler, or package manager — just plain HTML, CSS, and JavaScript served directly.

## Development

Open `index.html` directly in a browser or use any local server (e.g., `python3 -m http.server`). There is no build step, no linting, and no tests.

## Architecture

- **index.html** — Single-page layout with all content inline. Uses Tailwind CSS via CDN (`cdn.tailwindcss.com`) with a custom theme config embedded in `<script>`. Sections: Navigation, Hero, About, Skills, Projects, Contact, Footer.
- **style.css** — Custom styles that complement Tailwind: CSS reset, custom shadows (`shadow-soft`, `shadow-hover`), hero gradient background, scroll-reveal animations, card hover effects, navbar scroll state, mobile hamburger animation, and staggered transition delays.
- **script.js** — Vanilla JS with no dependencies. Handles: scroll-reveal via `IntersectionObserver` (`.scroll-reveal` → `.visible`), navbar shadow on scroll, smooth anchor scrolling, and mobile menu toggle.

## Key Conventions

- The site language is Korean (`lang="ko"`). Content text is in Korean; section headings and labels use English.
- Tailwind custom colors: `primary` (#1A1A1A), `accent` (#4A6CF7), `subtle` (#6B7280), `surface` (#F6F8FC), `surface-blue` (#EDF1FF). These are defined in the inline `tailwind.config` in `index.html`.
- Font: Inter (loaded from Google Fonts).
- Scroll animations use the `.scroll-reveal` class (CSS transition-based, toggled by JS IntersectionObserver) and `.reveal-up` class (CSS keyframe-based, for hero section initial load).
