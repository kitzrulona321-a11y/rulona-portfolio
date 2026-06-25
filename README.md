# Kitz Rulona — Portfolio Site

A fast, static portfolio built with [Astro](https://astro.build), deployed free to
**rulona.vercel.app**. Showcases two Claude automotive workflow case studies, skills,
and résumé.

## Run locally

```bash
cd site
npm install
npm run dev        # http://localhost:4321
```

Build a production bundle:

```bash
npm run build      # outputs to dist/
npm run preview    # serve the built site locally
```

## Deploy to Vercel (free)

1. Push this repo to GitHub (under `github.com/kitzrulona321-a11y`).
2. Go to [vercel.com](https://vercel.com) → **New Project** → import the repo.
3. If the repo root isn't the site, set **Root Directory** to `site`. Vercel
   auto-detects Astro (build: `npm run build`, output: `dist`). Click **Deploy**.
4. In **Settings → Domains**, add `rulona.vercel.app`.

Netlify and GitHub Pages work too — Astro outputs plain static files in `dist/`.

## Structure

```
site/
├─ src/
│  ├─ layouts/Base.astro              # HTML shell, nav, footer, SEO
│  ├─ pages/
│  │  ├─ index.astro                  # hero · about · skills · work · résumé · contact
│  │  └─ case-studies/
│  │     ├─ service-triage.astro
│  │     └─ lead-qualification.astro
│  └─ styles/global.css               # design system (gold + charcoal)
└─ public/
   ├─ favicon.svg
   └─ resume/Kitz-Rulona-Resume.html  # linked from the résumé section
```

## Before you go live

- **Add the résumé PDF:** export `resume/resume.html` to PDF (Ctrl+P → Save as PDF)
  and save it as `public/resume/Kitz-Rulona-Resume.pdf` so the "Download PDF" button
  resolves.
- **Headshot (optional):** drop a square photo in `public/` and replace the `KR`
  monogram `<div class="avatar">` in `src/pages/index.astro` with
  `<img class="avatar" src="/your-photo.jpg" alt="Kitz Rulona" />`.
- **Publish the demo repos** so the GitHub link has real projects behind it.
