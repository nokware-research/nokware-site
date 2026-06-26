# Nokware Research Solutions — Marketing Site

> **Purpose-built clinical trial technology rooted in equity, transparency, and open science.**

[![Deployed on Cloudflare Pages](https://img.shields.io/badge/Cloudflare%20Pages-Live-orange?logo=cloudflare&logoColor=white)](https://nokware-site.pages.dev)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Backup-blue?logo=github)](https://nokware-research.github.io/nokware-site)
[![License: MIT](https://img.shields.io/badge/License-MIT-teal.svg)](LICENSE)

---

## Live URLs

| Environment | URL |
|---|---|
| **Primary (Cloudflare Pages)** | https://nokware-site.pages.dev |
| **Backup (GitHub Pages)** | https://nokware-research.github.io/nokware-site |
| **Custom domain (pending)** | https://nokware-research.org |

---

## What's on the Site

A single-page marketing site with seven sections:

| Section | Description |
|---|---|
| **Hero** | Headline, trust badges, dual CTA launches e-Delegate app |
| **The Problem** | Exclusionary design, fragmented compliance, opacity in clinical research |
| **Our Approach** | Equity-first, open-by-default, compliance without compromise |
| **e-Delegate** | Feature showcase, live app CTA banner, browser UI mockup, compliance bar |
| **Developers** | GitHub repo card, contribute section, accurate tech stack |
| **About** | Founder bio (Kojo A. Quansah Jr., PharmD), values, CTA |
| **Footer** | Nav links, contact info, Launch App link |

---

## Tech Stack

| Tool | Purpose |
|---|---|
| Plain HTML + Tailwind CSS (CDN) | All styling, zero build step |
| Inter (Google Fonts) | Typography |
| Inline SVG | All icons, no external icon libraries |
| Cloudflare Pages | Primary hosting with CI/CD |
| GitHub Actions | Backup CI for GitHub Pages |

---

## Deploying Changes

Every push to `main` automatically redeploys the site on Cloudflare Pages in ~30 seconds and GitHub Pages in ~60 seconds.

That's it. Both deployments trigger automatically.

---

## Local Development

No build tools needed. Pick any option:

**Option 1 - Python (built into macOS/Linux, available on Windows)**

    python3 -m http.server 8080
    Open http://localhost:8080

**Option 2 - Node (no install required)**

    npx serve .
    Open the URL shown in your terminal

**Option 3 - VS Code**
Install the **Live Server** extension, right-click `index.html`, then Open with Live Server.

---

## Editing Content

All content lives in `index.html`. Each section has a matching HTML id:

| Section | ID to find in index.html |
|---|---|
| Hero | id="hero" |
| The Problem | id="problem" |
| Our Approach | id="approach" |
| e-Delegate | id="edelegate" |
| Developers | id="developers" |
| About / Footer | id="about" |

To update the e-Delegate app link, search for `e-delegate.qrx-jay.workers.dev` and replace with your custom domain once `nokware-research.org` is live.

---

## Brand Colors

| Token | Hex | Use |
|---|---|---|
| nokware-navy | #0A1628 | Hero, dark sections, footer |
| nokware-teal | #0D9488 | Primary CTAs, accents, links |
| nokware-gold | #D97706 | Secondary accent, badge labels |
| nokware-light | #F0FDF9 | Light section backgrounds |
| nokware-muted | #64748B | Supporting copy |

Colors are defined in the Tailwind config block at the top of `index.html`.

---

## Security

Security is applied in two layers:

**Layer 1 - HTML meta tags (active everywhere)**
- Content Security Policy (CSP)
- X-Frame-Options: DENY
- X-Content-Type-Options: nosniff
- Referrer-Policy
- Permissions-Policy (camera, mic, geolocation, payment, USB all blocked)

**Layer 2 - _headers file (active on Cloudflare Pages)**
- Strict-Transport-Security (HSTS) 2-year preload
- Cross-Origin-Opener-Policy
- Cross-Origin-Resource-Policy
- Cache control headers

---

## Custom Domain Setup

Once `nokware-research.org` is registered at Cloudflare Registrar:

1. Go to Cloudflare Pages, nokware-site, Custom Domains
2. Click Set up a custom domain, enter nokware-research.org
3. Cloudflare handles DNS automatically since it is also the registrar
4. HTTPS is provisioned automatically, no configuration needed

---

## Contact

- **Email:** inquiries_requests@nokware-research.org
- **Phone:** +1 (214) 473-4241
- **GitHub Org:** https://github.com/nokware-research
- **e-Delegate App:** https://e-delegate.qrx-jay.workers.dev

---

## License

MIT - open source, free to use, fork, and adapt.

---

Built by Kojo A. Quansah Jr., PharmD - Senior Clinical Research Associate and Founder of Nokware Research Solutions.
