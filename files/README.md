# Soofi Sons & Co. — Website

Official website for **Soofi Sons & Co.**, an eye care, optical, and hearing aid shop in Faisalabad, Pakistan, established in 1952.

🔗 Live site: [soofi-sons.vercel.app](https://soofi-sons.vercel.app)

## About

Soofi Sons & Co. (also spelled Sufi Sons) is a family-run business at 33 Katchery Bazar, near the Clock Tower in Faisalabad, offering:

- Eye Care / Eye Examinations
- Opticians & Prescription Eyewear
- Contact Lenses
- Hearing Aids

This site is a single-page, static site — no build step, no framework, no dependencies.

## Project structure

```
.
├── index.html      # entire site — markup, styles, and scripts in one file
├── favicon.svg      # browser tab icon (green circle + eye mark)
├── robots.txt        # crawler rules for search engines
├── sitemap.xml        # sitemap for search engine indexing
└── README.md         # this file
```

## Tech

- Plain HTML, CSS, and vanilla JavaScript — no build tools required
- Google Fonts: Fraunces (display), Inter (body), IBM Plex Mono (labels/numbers)
- Embedded Google Maps iframe for location
- Contact form submits as a pre-filled WhatsApp message (`wa.me` link)
- Schema.org `Optician` structured data (JSON-LD) for local SEO

## Running locally

No build step — just open the file directly, or serve it so relative paths (like the favicon) resolve correctly:

```bash
# option 1: just open it
open index.html          # macOS
start index.html         # Windows

# option 2: serve it (recommended, avoids any relative-path quirks)
npx serve .
# or
python3 -m http.server 8000
```

## Deployment (Vercel)

This repo is already connected to Vercel and deploys automatically on every push to `main`.

To deploy manually or set up a new project:
1. Push this repo to GitHub.
2. On [vercel.com](https://vercel.com) → **Add New → Project → Import Git Repository**.
3. No build settings needed — it's detected as static HTML.
4. Click **Deploy**.

## Updating content

Everything lives in `index.html`:
- **Contact info / phone / hours** — search for the `#location` and `#contact` sections.
- **Services** — the four cards under `#services`.
- **Colors / fonts** — CSS custom properties at the top of the `<style>` block (`:root`), e.g. `--green-deep`, `--gold`.
- **SEO meta tags & structured data** — inside `<head>`, including the `application/ld+json` block with address, phone, hours, and review rating.

## SEO checklist

- [x] Descriptive title & meta description
- [x] Open Graph / Twitter meta tags
- [x] `Optician` structured data (JSON-LD) with address, hours, phone, and aggregate rating
- [x] `robots.txt` + `sitemap.xml`
- [x] Favicon
- [ ] Custom domain (currently on `soofi-sons.vercel.app` — update canonical URL, Open Graph URLs, and sitemap once a real domain is connected)
- [ ] Google Business Profile claimed & linked to this site
- [ ] Submitted to Google Search Console

## License

Private business site — all rights reserved to Soofi Sons & Co.
