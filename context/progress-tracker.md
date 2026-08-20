# Progress Tracker

## Current Phase

- **WaterWatch v0.2.0 (development):** full-stack foundation built and pushed to
  `Team-Compass-2026/waterwatch`. Backend runs on the **career-gps stack**
  (Prisma 7 + `@prisma/adapter-pg` + Neon Postgres + Better Auth + Zod 4), all
  pages are wired to the query/API layer (with sample-data fallback), and a
  shared **design system** (4-level risk, fonts, tokens, live preview) is
  documented for both delivery paths. Theme classified for DEEP 2026: **Health
  and Wellbeing** (primary) + **Community Resilience and Sustainability**
  (secondary) → `waterwatch/docs/scope.md`.

## Current Goal

- Provision the Neon project + `DATABASE_URL` / `BETTER_AUTH_SECRET` /
  `BETTER_AUTH_URL`, run `prisma migrate deploy` + seed, and take the main app
  off sample data
- Build the Lovable design-system library per `waterwatch/docs/lovable/design-system-build.md`
- Complete the citizen verify flow (Confirm/Dispute) against
  `/api/reports/[id]/verify`

## Completed (WaterWatch brand identity sync)

- **Brand identity sync** across six-file context: added brand descriptor (*Turning community observations into early warnings for waterborne-disease risk*) and WATERWATCH (all-caps) brand mark for stylized/hero contexts. Parent repo commit `docs(context): sync WaterWatch brand descriptor and WATERWATCH brand mark`; app repo commit `chore(app): sync WaterWatch brand descriptor in metadata, manifest, README`.
- **Navy-dominant re-theme** (C1–C6): New palette — Primary Deep Navy `#123B5D`, Secondary Water Blue `#2F80ED`, Accent Coral Red `#EB5757`. shadcn/ui primitives added. All components migrated from `water-*` tokens. `/design-system` page removed. Lovable prompts + docs aligned with brand design spec. Favicon transparency fixed, maskable icons regenerated with navy bg. Fonts unchanged (Space Grotesk / DM Sans / Geist Mono).

## Completed (WaterWatch pivot — stack + design system)

- **App repo live** (`Team-Compass-2026/waterwatch`, pushed through commit
  `cf76e2a`): Next.js 16.3.1 + Turbopack, React Leaflet 5 + OSM, Tailwind v4.
  All 12 routes (`/`, `/home`, `/report`, `/map`, `/alerts`, `/profile`,
  `/dashboard`, `/design-system`, 3 API routes) build + lint + smoke-test clean.
- **Backend foundation** (`ef97096`): swapped off Supabase to the career-gps
  stack. `prisma/schema.prisma` (Better Auth + Area/Report/ReportVerification/
  RiskScore/Alert/Organization/OrgMember/OrgSubscription), `prisma.config.ts`,
  `prisma/seed.ts`, generated client in `lib/generated/prisma`. API:
  `/api/auth/[...all]`, `/api/reports` (POST create + GET feed, zod, rate limit),
  `/api/reports/[id]/verify`. Lib: `prisma.ts` (DB-aware with fallback),
  `auth.ts`, `auth-client.ts`, `session.ts`, `risk.ts` (deterministic 4-level
  engine), `queries.ts` (async data layer auto-falling back to sample data).
- **Page wiring** (`dd981aa`, parallel subagents): Landing + Map, Report form +
  Alerts, Home + Profile + Dashboard all read from `lib/queries.ts` /
  `/api/reports`. `/profile` is server-dynamic (auth session); rest static.
- **Design system**: `docs/design-system.md` (canonical), fonts Space Grotesk / DM Sans / Geist Mono, clean & airy
  tokens, **4-level risk scale** adopted app-wide (CRITICAL 85–100 `#b91c1c`,
  HIGH 67–84 `#dc2626`, MODERATE 34–66 `#d97706`, LOW 0–33 `#16a34a`).
- **Lovable prompts** (`cf76e2a`): all 7 page prompts updated to the 4-level
  scale + design-system pointers; `docs/lovable/design-system-build.md` holds
  the Lovable design-system library build plan.
- **Dual delivery path** documented: main app = Prisma/Neon/Better Auth;
  Lovable = Supabase (`supabase/migrations/0001_init.sql`, `seed.sql`).

## Completed (Career GPS heritage — retained in git history)

- Previous project: Career GPS — AI-powered career navigation platform
  (Next.js 16 + Prisma + Hono + Better Auth + Neon + RAG coach). All prior
  milestones, seed data, migrations, and deployed routes remain in git history
  and the `career-gps` repo, now archived as reference (and the stack source
  for WaterWatch).

## In Progress

- Neon provisioning + env: needs `DATABASE_URL`, `BETTER_AUTH_SECRET`,
  `BETTER_AUTH_URL` (a local `.env` — not committed)
- Verifying the report-create / verify flows end-to-end against a real DB
- Parent org repo context/spec sync (this tracker + `context/specs/*`)

## Next Up (when build resumes)

- Create Neon project + branch, run `prisma migrate dev --name init` +
  `prisma db seed`; set env vars; re-run build + smoke test
- Seed the 5 pilot areas; verify `/api/reports` POST and `[id]/verify` in dev
- Build the Lovable design-system library (tokens → waves 1–4 → showcase)
  per `docs/lovable/design-system-build.md`
- Optional: enforce org membership/RBAC for `/dashboard`

## Open Questions

- Which 2–3 Yangon townships for the pilot (currently 5 seeded areas)?
- Anonymous vs signed-in split for the pilot demo
- Adopt the org account flow now, or keep `/dashboard` demo-only for DEEP?
- Build the Lovable design-system library now, or after the main app demo?

## Architecture Decisions

- Community-powered WASH early warning · Team Compass 2026
- **Main app:** Prisma 7 + `@prisma/adapter-pg` + Neon Postgres + Better Auth +
  Zod 4 (career-gps stack, mirrored) — pages fall back to sample data until DB
  is configured
- **Lovable path:** Supabase (Postgres + Auth + Storage + RLS) per
  `supabase/migrations/0001_init.sql`
- Maps: React Leaflet 5 + OpenStreetMap (no Mapbox key needed)
- Deterministic, explainable 4-level risk engine (no LLM in the core math)
- Design system shared across both stacks: 4-level risk, Space Grotesk + DM
  Sans + Geist Mono, clean & airy, "reports are signals, not diagnoses"
- Anonymous reporting always possible; `/profile` auth-aware

## Session Notes

- Full-stack foundation completed in one push: stack swap, schema, backend,
  API routes, page wiring (parallel subagents), design system + docs, Lovable
  prompts — three commits pushed (`ef97096`, `dd981aa`, `cf76e2a`).
- The generated Prisma client (`lib/generated/prisma`) is committed (24 files)
  so the repo builds without a generate step.
- Remaining before live demo: Neon provisioning + env + seed; optional Lovable
  design-system library build.
- Brand identity sync (descriptor + WATERWATCH brand mark) committed across
  parent repo context files and waterwatch app metadata/manifest/README.