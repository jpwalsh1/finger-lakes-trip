# Exploring the Finger Lakes — Walsh Family Trip

A single-page trip itinerary, styled as a vintage travel-poster / postcard
site, for the Walsh family's Thursday–Sunday trip to a lakefront cottage
on Keuka Lake, NY.

**Live site:** enable GitHub Pages (see below) and it'll be at
`https://<your-username>.github.io/finger-lakes-trip/`

## What's in here

- `index.html` — the whole site (single file, no build step)
- `CLAUDE.md` — notes for Claude Code if you want AI help editing this repo
- `MEMORY.md` — trip facts (dates, addresses, restaurant picks, driving notes)
- `.github/workflows/pages.yml` — auto-deploys to GitHub Pages on every push to `main`

## Setting up GitHub Pages (one-time)

After pushing this repo to GitHub:

1. Go to the repo on GitHub → **Settings** → **Pages**
2. Under "Build and deployment", set **Source** to **GitHub Actions**
3. Push to `main` (or re-run the workflow from the **Actions** tab) — the
   included workflow will build and deploy automatically
4. The live URL will show up in the **Pages** settings page and in the
   Actions run summary, typically
   `https://<your-username>.github.io/<repo-name>/`

No further setup needed — every push to `main` redeploys automatically.
