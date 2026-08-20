# Progress Tracker

## Current Phase

- **WaterWatch v0.1.0 (development):** MVP shell built and live in the
  `waterwatch` repo (`Team-Compass-2026/waterwatch`), running on sample data
  (Next 16 + React Leaflet/OSM). Theme classified for DEEP 2026: **Health and
  Wellbeing** (primary) + **Community Resilience and Sustainability**
  (secondary) → `waterwatch/docs/scope.md`. Six-file context, setup/scope docs,
  and per-page **Lovable prompts** shipped in `waterwatch/docs/lovable/`.

## Current Goal

- Finalize WaterWatch spec + prototype brief + tech selection (Supabase, Mapbox/
  Google Maps, mobile-first frontend)
- Establish pilot scope (2–3 Yangon townships) and MVP vertical:
  report → map → verify → risk score → citizen alert / org dashboard

## Completed (WaterWatch pivot)

- **WaterWatch app repo created and pushed** (`Team-Compass-2026/waterwatch`):
  Next.js 16.3.1 (no `src/`), React Leaflet 5 + OpenStreetMap, Tailwind v4;
  MVP routes `/` `/home` `/report` `/map` `/alerts` `/profile` `/dashboard`;
  `bun run build` + `lint` clean
- **Six-file context + project.yaml added to the app repo** (`waterwatch/context/*`,
  `project.yaml` v0.1.0 dev, release `drop`)
- **Scope documented for DEEP 2026 theme:** Health and Wellbeing (primary) +
  Community Resilience and Sustainability (secondary) → `waterwatch/docs/scope.md`
- **Setup runbook** added → `waterwatch/docs/setup.md`
- **Lovable prompts per page** (7 pages + shared context + map/SSR notes) →
  `waterwatch/docs/lovable/`
- Product reframed from Career GPS to **WaterWatch**:
  *See the risk. Share the signal. Protect the community.*
- Canonical master spec saved: `context/product-spec.md` (50 sections: problem,
  gap, users, solution, six-step flow, incentive model, research, product,
  business model, MVP, pilot budget, GTM, pitch)
- `project-overview.md` rewritten to the WaterWatch framing (Observe → Report →
  Verify → Analyze → Alert → Prioritize)
- Prototype brief saved: `context/prototype-spec.md` (citizen app: Landing →
  Home → Report → Map → Alerts → Profile; + Organization Dashboard)
- `architecture.md` rewritten: Supabase (Postgres + PostGIS + Auth + Storage +
  Realtime), Mapbox/Google Maps, deterministic explainable risk engine,
  anonymous reporting, RLS invariants
- `ui-context.md` rewritten: water-blue brand, risk semantics (green/amber/red
  with badge + label, never color alone), mobile-first citizen app + desktop
  org dashboard
- `code-standards.md` + `ai-workflow-rules.md` updated to the new stack and
  signals-not-diagnoses principle
- README + org profile updated to WaterWatch
- Problem statistics carried over and validated (WHO Yangon AWD outbreak 2024,
  UNICEF WASH assessment, mWater precedent)

## Completed (Career GPS heritage — retained in git history)

- Previous project: Career GPS — AI-powered career navigation platform
  (Next.js 16 + Prisma + Hono + Better Auth + Neon + RAG coach). All prior
  milestones, seed data, migrations, and deployed routes remain in git history
  and the `career-gps` repo, now archived as reference.

## In Progress

- Decide product repo plan: repurpose `career-gps` repo (renamed `waterwatch`)
  vs. fresh scaffold
- Finalize report categories, township baseline data, and risk-score formula for
  the MVP vertical

## Next Up (when build resumes)

- Scaffold WaterWatch app (mobile-first, Supabase backend)
- Supabase project + schema + RLS + PostGIS setup; seed 2–3 pilot townships
- MVP vertical: report (anonymous + signed-in) → map → verify → basic risk
  score → citizen alert / org dashboard
- Demo path for evaluators: report a WASH problem → see it verified → risk
  updates → alerts + org dashboard view

## Open Questions

- Which 2–3 Yangon townships for the pilot?
- Anonymous vs signed-in split for the pilot demo
- Risk-score weighting (volume vs cluster vs verification vs signal mix)
- Reuse existing `career-gps` codebase/skills or start fresh (Supabase vs Neon)

## Architecture Decisions

- Community-powered WASH early warning · Team Compass 2026
- Supabase (Postgres + PostGIS + Auth + Storage + Realtime) for the MVP
- Mapbox / Google Maps for maps
- Mobile-first citizen app + desktop organization dashboard
- Deterministic, explainable risk engine (no LLM in the core math for MVP)
- Reports are signals, not diagnoses; anonymous reporting always possible

## Session Notes

- Full pivot executed in a single pass: all 6 context files + specs + org
  profile + README rewritten from Career GPS to WaterWatch
- Career GPS heritage preserved as a reference section in `project-overview.md`
  and in git history — nothing was deleted from the repo, only rewritten
- MVP stays at five things (report, map, verify, basic risk score, two views)
- Do not scaffold further until user says **build**