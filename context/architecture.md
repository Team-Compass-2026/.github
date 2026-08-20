# Architecture Context — WaterWatch

> Product ground truth: `context/product-spec.md` (master spec) and
> `context/project-overview.md`. **MVP = deterministic, explainable risk
> scoring over community reports + verification. No medical diagnosis, no
> epidemiological inference engine in v1.**

## Dual-path build

WaterWatch ships on **two parallel implementations** (locked in
`project.yaml`, `docs/setup.md`):

1. **Main app — Next.js + Neon** (`waterwatch/`, this repo): production-quality
   backend with Prisma 7 + Neon Postgres, Better Auth, Hono API, React Query.
2. **Prototype — Lovable + Supabase** (`docs/lovable/` prompts + `supabase/`
   migrations): fast-build citizen app + org dashboard for demos.

This doc describes the **main app**. The Lovable/Supabase path mirrors the same
data model with Supabase Auth, PostGIS and Realtime.

## Stack (main app)

| Layer | Technology | Role |
| ----- | ---------- | ---- |
| Frontend | Next.js 16 (root `app/`, no `src/`) + TypeScript | Citizen app + org dashboard |
| API | **Hono** (catch-all route `app/api/[[...route]]/`) | Report feed / create / verify |
| Client data | **TanStack Query** + typed Hono client (`hc<AppType>`) | Server state |
| Auth | **Better Auth** (email/password, cookie sessions) | Sessions / identity |
| Database | **Prisma 7** (`@prisma/adapter-pg`) → **Neon Postgres** | Reports, verifications, areas, alerts, users |
| Risk engine | `lib/risk.ts` (deterministic, explainable) | Volume, cluster, verification, signal mix, recency |
| Maps | **React Leaflet** + OpenStreetMap (free tiles, no key) | Neighborhood map + area overlays |
| Edge logic | Next 16 **`proxy.ts`** | Security headers + API CORS allowlist |
| Files | (not wired) — photo upload is local preview only | Report photos (next) |
| Hosting | Vercel + Neon | Hackathon deploy |

## System Boundaries

- `app/` — citizen routes: `/`, `/home`, `/report`, `/map`, `/alerts`,
  `/profile`, `/sign-in`, `/sign-up`, `/design-system`
- `app/(org)/dashboard` — organization WASH Intelligence dashboard
- `app/api/[[...route]]/` — Hono app (`route.ts` + `reports.ts`); Better Auth
  at `app/api/auth/[...all]/`
- `features/reports/api/` — React Query hooks (feed, create, verify)
- `lib/` — `prisma.ts`, `queries.ts`, `risk.ts`, `auth.ts`/`auth-client.ts`/
  `session.ts`, `data.ts` (sample fallback), `api/hono-client.ts`
- `prisma/` — `schema.prisma`, `seed.ts`, `prisma.config.ts`
- `proxy.ts` — Next 16 built-in proxy
- `supabase/` — Lovable path (migrations + seed.sql)
- `context/` + `docs/` — product ground truth

## Storage Model

- **Postgres (Neon):** `User`, `Account`, `Session`, `Verification` (Better
  Auth) · `Report` (type, lat/lng, description, `whenHappened`,
  `isAnonymous`, `userId?`, `areaId?`) · `Area` (name, lat/lng, `radiusM`,
  `baselineReportsPerWeek`) · `ReportVerification` (`confirm`/`dispute`/
  `not_sure`) · `Alert` (`moderate`/`high`)
- **Geospatial:** plain `lat`/`lng` doubles + haversine distance in the risk
  engine (no PostGIS in the main app; PostGIS is available on the Supabase
  path)
- **Baseline:** per-area `baselineReportsPerWeek` so current activity is
  compared to normal

## Auth and Access Model

- **Better Auth** email/password; cookie session `better-auth.session_token`
- **Anonymous reporting** = `isAnonymous` flag / nullable `userId`
- **Citizen role:** create reports, verify/dispute, receive alerts, view risk
- **Organization role:** read aggregated risk + underlying reports (dashboard
  is currently open; org gating is next)
- Reports are **signals, not diagnoses** — no health data fields beyond the
  "illness cluster" category

## Risk engine (non-LLM core)

Deterministic, explainable WASH Risk Score per area (0–100), `lib/risk.ts`:

- **Volume vs baseline** — report count vs the area's weekly normal
- **Cluster density** — reports concentrated within ~1.2 km of area center
- **Verification confidence** — independent confirms vs disputes
- **Signal mix** — diversity of report types
- **Recency** — exponential decay (72 h half-life) so old reports fade

Output includes a per-component breakdown so every score answers *"why did this
change?"* Scores are recomputed on demand from the DB (`lib/queries.ts`).

## Scaling & Performance Constraints

- Pilot: hundreds to low thousands of users, 2–3 townships
- Risk score refresh: computed per request on demand (fine at pilot scale;
  scheduled/incremental later)
- Data volume: small for MVP (thousands of reports) — indexed queries suffice

## Invariants

1. Reports are **signals, not diagnoses** — never claim an outbreak/diagnosis.
2. Risk scores are transparent and explainable (component breakdown).
3. Anonymous reporting must always be possible.
4. PII is minimized; identity/contact data never exposed to organizations.
5. Verification + clustering gate outlier reports (duplicate/misinformation
   handling).
6. No secrets in git; `.env` is gitignored, `.env.example` documents the vars.
7. Next 16 conventions differ from training data — read
   `node_modules/next/dist/docs/` before writing Next code (proxy, SSR rules).

## MVP Vertical

`report (anonymous or signed-in) → appears on map → nearby user verifies →
risk score updates → citizen alert / org dashboard view`

Version 1 is five things only: report, map, verify, basic risk score, two views.