# Nimesh Gautam — Academic Portfolio

A static, single-page academic portfolio for Nimesh Gautam (AI Engineer & Researcher).
Editorial/scholarly design: Spectral serif type, IBM Plex Sans labels, a restrained
paper-and-ink palette, light/dark themes, and five accent colors.

## Structure

```
.
├── index.html                 # The entire site (inline CSS + JS, self-contained)
├── assets/
│   ├── profile.jpeg           # Headshot used in the hero
│   ├── profile-academic.svg   # SVG fallback if the photo fails to load
│   └── profile.svg
└── .do/app.yaml               # DigitalOcean App Platform static-site spec
```

The page is fully static — no build step, no dependencies. Open `index.html`
directly in a browser to preview.

## Deploy to DigitalOcean App Platform (static site, free tier)

This repo includes a `.do/app.yaml` static-site spec. To deploy:

1. Push to GitHub (`gtmbuddha2/nimesh-website`, branch `main`).
2. In the DigitalOcean control panel: **Apps → Create App → GitHub**, select this
   repo. It is detected as a static site (no build command, output dir `/`).
   `deploy_on_push` is enabled, so every push to `main` redeploys automatically.

Alternatively, with `doctl`:

```bash
doctl apps create --spec .do/app.yaml
```

## Editing content

All content lives in `index.html`. To change the headshot, replace
`assets/profile.jpeg`.
