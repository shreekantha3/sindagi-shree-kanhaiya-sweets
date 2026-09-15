# TEST REPORT — Shree Kanhaiya Sweets And Snacks
> Date: 2026-09-10 | Tester: Senior Engg | Segment: Food | Tier-2 (no phone in CSV)

## Build
- [x] `npm run build` PASS (vite 5.4.21, 4 modules, 0 warnings)
- dist sizes: 12.61 kB HTML / 12.31 kB CSS / 1.20 kB JS — well under perf budget (<200KB JS, <1.5MB total)
- dist base paths verified: `/sindagi-shree-kanhaiya-sweets/assets/*` + favicon.svg copied

## Static checks (all PASS)
- [x] NO tel:/wa.me/+91 anywhere (grep CLEAN) — CSV phone empty, never invented
- [x] Directions/Maps CTAs only: nav, hero, visit, mobile floating button all → Google Maps URL
- [x] data-missing flags present (3× — phone hero banner, phone/hours visit note, area-level address note)
- [x] JSON-LD CandyStore (no telephone key) + PostalAddress + AggregateRating 5.0
- [x] H1 sweets angle, semantic sections, skip link, async fonts (media=print onload)
- [x] No lorem ipsum, no invented hours/prices/address (area-level address honestly flagged)
- [x] aria-expanded on nav toggle, keyboard reachable CTAs, contrast-safe palette (pilot copy)

## Pending (requires preview + device lab before Deployed)
- [ ] Lighthouse CI mobile+desktop (target 90/95/95/95)
- [ ] Playwright 12-case E2E + axe (0 serious) + linkinator
- [ ] Screenshots 360/768/1440 attached to PR
- [ ] GitHub Pages deploy verify (200 + base path assets)

## Verdict: BUILT + STATIC QA PASS → ready for full QA + separate repo deploy

## Maps embed + README (2026-09-15)
- [x] Google Maps iframe embed added to #visit panel (lazy-loaded, `output=embed`, query fused from page's own Maps URL)
- [x] Per-site README.md added (live link, owner update guide)
