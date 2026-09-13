# Roots & Remedies Site — Project Overview

## What this is
Bilingual (EN/NL) website for **Roots & Remedies**, a Dutch foundation
(stichting) stewarding an ecosystem of regenerative experiments in food,
land, energy, and governance. Built with Next.js (App Router) and Tailwind.

## Routing
- `/` redirects to `/en` (see `src/app/page.tsx` and `src/middleware.ts`).
- All content lives under a language segment `/[lang]`, where `lang` is `en` or `nl`.
- Pages under `/[lang]`: mission, ecosystem, projects (+ project detail),
  journal (+ post detail), contact.

## Where to edit content
- Site config (name, domain, contact, nav): `src/lib/site.ts` and `src/content/site.ts`
- Translations / UI copy dictionaries: `src/content/i18n.ts`
- Ecosystem & projects data: `src/content/ecosystem.ts`
- Journal posts (MDX): `src/content/journal/{en,nl}/*.mdx`
- Language pages: `src/app/[lang]/*/page.tsx`

## Key UI / layout files
- Root layout: `src/app/layout.tsx`
- Language layout (header/footer wrapper): `src/app/[lang]/layout.tsx`
- Global styles: `src/app/globals.css`
- Site components: `src/components/site/*` (SiteHeader, SiteFooter, LanguageToggle,
  Card, Badge, PageHeader, MDXComponents)
- Helpers: i18n `src/lib/i18n.ts`, journal loading `src/lib/journal.ts`,
  metadata/JSON-LD `src/lib/metadata.ts`

## Machine-readable endpoints
- `src/app/feed.json/route.ts`, `src/app/meta.json/route.ts`,
  `src/app/sitemap.ts`, `src/app/robots.ts`

## Domain
- Production: **`rootsandremedies.nl`** (the earlier `rootsandremedies.earth`
  domain is retired). Attaching the domain to the Vercel project is a
  deploy-time step.

## Current TODOs
- Replace placeholder OG image referenced in `src/content/site.ts` / `src/lib/site.ts`.
- Populate `src/app/feed.json/route.ts` with real items if the journal feed changes.
- Copy polish across the EN/NL dictionaries in `src/content/i18n.ts`.

## Local dev
```bash
npm install
npm run dev
```

## Build / lint / typecheck
```bash
npm run lint
npm run typecheck
npm run build
```

## Deployment
See `DEPLOYING.md` for Vercel steps.

## Codex operating rules
See `CODEx-RULES.md`.
