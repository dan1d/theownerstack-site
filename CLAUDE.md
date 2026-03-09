# AutoBooks — Marketing Site

## Overview
Static marketing landing page for AutoBooks, the automated bookkeeping SaaS. Showcases features, pricing, and drives sign-ups to the main app.

## Tech Stack
- **Framework:** Astro 5.17.1 (static output, strict TypeScript)
- **Styling:** Tailwind CSS 4.1.18 (via Vite plugin)
- **Fonts:** Inter (variable), JetBrains Mono
- **Hosting:** Cloudflare Pages (via wrangler)
- **CI/CD:** GitHub Actions → Cloudflare Pages deploy on push to `main`
- **Support Widget:** Chatwoot embedded chat

## Key Commands
```bash
npm install          # Install dependencies
npm run dev          # Dev server on localhost:4321
npm run build        # Build static site to ./dist
npm run preview      # Preview built site locally
```

## Project Structure
- `src/components/` — Astro components (Hero, Navbar, Footer, ProductCard, etc.)
- `src/layouts/Layout.astro` — Base layout with SEO, JSON-LD, Chatwoot widget
- `src/pages/index.astro` — Single landing page (Hero → How It Works → Features → Pricing → CTA)
- `src/styles/global.css` — Theme variables, colors, shadows, animations
- `public/` — Static assets (favicon, OG image)
- `wrangler.toml` — Cloudflare Pages config (project: theownerstack-site)

## Page Sections
1. Navbar (sticky, mobile hamburger)
2. Hero — "Your Clover Sales, in QuickBooks, Every Morning"
3. How It Works (3 steps: Connect → Map → Automate)
4. Features (6 cards)
5. Benefits + "What syncs daily" reference
6. Pricing (Starter $15/mo, Growth $25/mo, Accountant Bundle $60/mo)
7. Footer CTA + Footer

## Design System
- **Primary:** Teal (#00d1b2 range)
- **Brand colors:** Clover (#4CAF50), QuickBooks (#2CA01C)
- Scroll reveal animations (respects prefers-reduced-motion)
- Mobile-first responsive design

## External Links
- **Production app**: https://autobooks.theownerstack.com
- Sign up/in CTAs → `autobooks.theownerstack.com`
- Chatwoot → `support.autobooks.theownerstack.com`

## Deployment
Push to `main` triggers GitHub Actions → `npm ci && npm run build` → Cloudflare Pages.
Requires secrets: `CLOUDFLARE_API_TOKEN`, `CLOUDFLARE_ACCOUNT_ID`.
