# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A gallery of radically different informational website designs for "Studio Aura" — a dance and fitness studio. Each page explores a distinct visual direction — same content, wildly different design. The gallery page (`index.html`) serves as the entry point linking all designs.

## Constraints

- **Strictly HTML and CSS only** — no JavaScript whatsoever
- Each landing page is self-contained: single `index.html` with embedded `<style>` blocks
- Images: use Unsplash source URLs (`https://images.unsplash.com/photo-{id}?w={width}&h={height}&fit=crop`) with dance/fitness-relevant photos, plus local images in `images/` directory
- Use CSS-only `<details>/<summary>` for expandable sections (dance forms, FAQs)
- Vary image density per design — some heavy, some moderate, some barely any

## Architecture

- `index.html` + `styles/gallery.css` — gallery page with cards linking to each design
- `pages/{number}-{slug}/index.html` — each landing page, self-contained
- `images/` — local studio/dance photos (studio-floor.png, studio-reception.png, ballet-dancer.png, dance-studio.png)
- Gallery card previews use CSS `::after` pseudo-elements with mood colors (defined in `gallery.css` as `.preview-{n}`)
- "Back to Gallery" links in each page point to `../../index.html`

## Required Content Per Landing Page

Each page must include:

1. Studio name "Studio Aura" displayed prominently
2. About section with location: "247 Movement Lane, Arts District, Downtown"
3. Dance forms & fitness styles (Ballet, Contemporary, Hip-Hop, Jazz, Salsa, Bollywood, Zumba, Yoga, Gymnastics) — expandable with details
4. Weekly class schedule (partial — not every slot filled)
5. Upcoming workshops section
6. FAQs section (experience, attire, registration, cancellation, private lessons, parking)
7. Contact & location section — Phone: (555) 234-8901, Email: hello@studioaura.com

## Adding a New Landing Page

1. Create `pages/{number}-{slug}/index.html` with embedded styles
2. Add a `.preview-{n}` style in `styles/gallery.css`
3. Add a card entry in `index.html` inside the `.gallery` grid

## Workflow

- Use parallel agents when building multiple pages simultaneously
- Each design should be wildly distinct: different layouts, moods, typography, spacing, color palettes, image density
- Take full creative freedom to explore all tastes and directions
