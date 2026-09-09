# Project

Static marketing site. Design source of truth is ./mocks/
No CMS, no database, no auth, no user accounts.

## Stack

- Astro 7 — static output only, no SSR adapters
- Tailwind CSS v4 — CSS-first, configured via @tailwindcss/vite
- Starwind UI — source-owned components in src/components/starwind/
- TypeScript strict

## Rules

- Tailwind v4 has no JS config. Design tokens live in src/styles/global.css
  under @theme. Never create tailwind.config.js.
- Use theme tokens. Arbitrary values (p-[13px], text-[#3a7]) need a reason.
- No React, Vue or Svelte. Interactivity = a Starwind component, or vanilla JS
  in a <script> tag. Nothing else.
- Before using a Starwind component, read its source in src/components/starwind/.
  Never guess props. Use `npx starwind@latest search` to find components,
  `npx starwind@latest add <name>` to install.
- Check src/components/ for an existing component before creating a new one.
- Mobile-first. Every section must work at 320px, 768px, 1280px and 1920px.
- Local images via astro:assets <Image />. Never a raw <img> for local files.
- Semantic HTML: one <h1> per page, real <nav>/<main>/<footer>, alt on every image.
- No localStorage, no analytics, no third-party scripts unless I ask.

## Working style

- Build one section at a time. Never generate a whole page in one pass.
- Show a plan before implementing anything non-trivial.
- Match the mockup's spacing and type precisely. Measure, don't approximate.
- If something in the mockup is ambiguous, ask rather than invent.

## Definition of done

`npm run build` and `npx astro check` both pass with zero errors.
