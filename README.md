Roots & Remedies — bilingual (EN/NL) foundation site built with Next.js (App Router) and Tailwind.

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open http://localhost:3000 with your browser. `/` redirects to `/en`; content
lives under `/[lang]` (`en` or `nl`).

Key editing entry points:
- Site config + domain/contact: `src/lib/site.ts`, `src/content/site.ts`
- Translations / UI copy: `src/content/i18n.ts`
- Language pages: `src/app/[lang]/*/page.tsx`
- Ecosystem & projects data: `src/content/ecosystem.ts`
- Journal posts (MDX): `src/content/journal/{en,nl}/*.mdx`

More context and handoff details: `PROJECT-OVERVIEW.md`.

## Deploy on Vercel
See `DEPLOYING.md`.
