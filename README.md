# AutoBooks — Marketing Site

Static marketing landing page for [AutoBooks](https://autobooks.theownerstack.com), the automated bookkeeping SaaS by TheOwnerStack.

## Tech Stack

- **Astro 5.17** (static output, strict TypeScript)
- **Tailwind CSS 4.1** (via Vite plugin)
- **Cloudflare Pages** (auto-deploy on push to `main` via GitHub Actions)

## Commands

```bash
npm install          # Install dependencies
npm run dev          # Dev server on localhost:4321
npm run build        # Build to ./dist
npm run preview      # Preview built site
```

## Structure

```
src/
├── components/      # Hero, Navbar, Footer, ProductCard, etc.
├── layouts/         # Base layout (SEO, JSON-LD, Chatwoot widget)
├── pages/           # index.astro (single landing page)
└── styles/          # Theme variables, colors, animations
```

## Deployment

Push to `main` → GitHub Actions → `npm ci && npm run build` → Cloudflare Pages.

Requires secrets: `CLOUDFLARE_API_TOKEN`, `CLOUDFLARE_ACCOUNT_ID`.

## Links

- **App**: https://autobooks.theownerstack.com
- **Site**: https://theownerstack.com
- **Support**: https://support.autobooks.theownerstack.com
