# Handoff — Roots & Remedies Site

## Project status
- Bilingual (EN/NL) site; `/` redirects to `/en`.
- Routes under `/[lang]`: mission, ecosystem, projects (+ project detail),
  journal (+ post detail), contact; plus `/meta.json`, `/feed.json`,
  `/sitemap.xml`, `/robots.txt`.
- SEO metadata and JSON-LD are built in `src/lib/metadata.ts`.
- Domain: production is **`rootsandremedies.nl`** (config updated; attaching the
  domain to the Vercel project is a deploy-time step). The older
  `rootsandremedies.earth` is retired.
- Contact email: `hello@rootsandremedies.nl`.

## Quick start
```bash
npm install
npm run dev
```

## Suggested next steps
1) **Brand assets**
   - Add a real OG image at `/public/og-image.png` (referenced from `src/lib/site.ts` / `src/content/site.ts`).
2) **Journal content**
   - Add or edit posts under `src/content/journal/{en,nl}/*.mdx`.
3) **Meta endpoint**
   - Review `src/app/meta.json/route.ts` if summary copy changes.
4) **Analytics / privacy**
   - Decide on analytics (Plausible, Umami, Vercel Analytics) and privacy policy placement.
5) **Content polish**
   - Refine EN/NL copy in `src/content/i18n.ts`; keep both languages in sync.
6) **QA checklist**
   - Language toggle, mobile nav open/close, focus states, contact form validation,
     and JSON-LD not visible in the UI.

## Key files to know
- Site config: `src/lib/site.ts`, `src/content/site.ts`
- i18n: `src/lib/i18n.ts`, `src/content/i18n.ts`
- Ecosystem/projects: `src/content/ecosystem.ts`
- Journal: `src/lib/journal.ts`, `src/content/journal/*`
- Layout + styles: `src/app/layout.tsx`, `src/app/[lang]/layout.tsx`, `src/app/globals.css`
- Components: `src/components/site/*`
- Machine endpoints: `src/app/meta.json/route.ts`, `src/app/feed.json/route.ts`

## Constraints reminder
- Roots & Remedies is a nonprofit foundation (stichting) that stewards an
  ecosystem of regenerative projects and shared intellectual property.
