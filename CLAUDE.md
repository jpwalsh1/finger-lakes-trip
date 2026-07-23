# CLAUDE.md

Project context for Claude Code (or any Claude session) working in this repo.

## What this repo is

A single-page trip itinerary site for the Walsh family's Finger Lakes long
weekend. It's a static HTML page (`index.html`) styled as a vintage
travel-poster / postcard itinerary, meant to be hosted for free on GitHub
Pages so the family can pull it up on their phones during the trip.

## Structure

- `index.html` — the entire site. Single file, inline `<style>`, a few
  inline SVG illustrations (lake/cabin/pines scene, wave dividers), Google
  Fonts (Fraunces + Inter + IBM Plex Mono) loaded via `<link>`. No build
  step, no JS framework, no dependencies to install.
- `MEMORY.md` — trip facts (dates, addresses, lodging, food picks, driving
  notes) that should stay in sync with what's actually in `index.html`.
  Treat this as the source of truth for trip details if the HTML and this
  file ever disagree — update both together.
- `.github/workflows/pages.yml` — GitHub Actions workflow that deploys the
  repo to GitHub Pages on every push to `main`.

## Editing conventions

- Keep it a single static HTML file. Don't introduce a bundler or
  framework for a page this size.
- Color tokens are defined as CSS custom properties at the top of the
  `<style>` block (`--lake`, `--burgundy`, `--gold`, `--cream`, etc.) —
  reuse those rather than hardcoding new hex values.
- Each day is a `.day` card with a `.stamp` (postmark-style date badge), a
  `table.sched` schedule table, and a `.food-block` listing food options.
  The top-recommended restaurant/spot in each `.food-list` gets the `top`
  class and a `★` — keep that pattern if adding new days or options.
- Mobile responsiveness matters — the family may pull this up on phones in
  the car. Test narrow viewports after changes.
- Respect `prefers-reduced-motion` if adding any animation.

## Deployment

Pages deploys automatically from `main` via the Actions workflow. No
manual build required — just push.
