# RightsKit — Launch TODO

Canonical checklist. Reference by number (e.g. "do 3", "status of 7").
Status: [ ] todo · [~] in progress · [x] done · [-] won't do

## Blockers (must-do before launch)
1. [-] **Contact form backend** — DEFERRED: wire up once the site is live. (Modal UI + validation done; submit just shows confirmation for now.)
2. [x] **Confirm production domain** — `rightskit.com` confirmed (astro.config + robots.txt).
3. [x] **Real OG share image** — branded 1200×630 at `public/og-image.jpg` (logo + tagline + purple hex).
4. [ ] **Host + security headers** — pick host (Netlify / Vercel / Cloudflare); add headers file (CSP, X-Frame-Options, Referrer-Policy, etc.) + deploy config.

## Should-do
5. [~] **Copy proofread** — no typos/grammar errors. Optional: reduce repetition of "untapped revenue today" (×4) and "unlicensed commercial UGC sync" (×3).
6. [x] **Favicon** — brand hex+plus mark: `favicon.svg`, multi-size `favicon.ico` (16/32/48), `apple-touch-icon.png` (180, navy tile).
7. [x] **Footer** — email + copyright + Privacy link (right-aligned). No socials/terms needed.
8. [x] **Real-device QA** — mobile pass on iPhone (LAN preview); menu, modal, layouts confirmed.

## Nice-to-have
9. [x] **Lighthouse pass** — Perf 97, A11y 100, Best Practices 100, SEO 100 (mobile, local preview; TBT 0ms, CLS 0).
10. [ ] **Cleanup `public/assets/` + `public/assets_FULL/`** — ~48MB dead weight shipping in the build (not referenced).
11. [ ] **Downsize remaining source images** — repo/build weight (served output already optimized).

## Done (this build)
- [x] Responsive pass (mobile layouts, fluid hero, sticky nav)
- [x] Performance: Inter subset (344→60KB), lazy hero images, font preloads, sound-waves as CSS, WebP
- [x] Mobile UGC banner served as a lightweight dedicated crop
- [x] SEO meta: canonical, Open Graph, Twitter, theme-color, robots.txt, sitemap generating
- [x] Custom 404 page
- [x] Accessibility: skip link, landmarks, decorative alts, reduced-motion, dialog focus-trap
- [x] Contact modal (email + message) on all CTAs, matches site button
- [x] Nav wiring (Services anchor, smooth scroll, Learn more → UGC)
