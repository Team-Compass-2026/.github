# Architecture Context — WaterWatch

> Product ground truth: `context/product-spec.md` (master spec) and
> `context/project-overview.md`. **MVP = deterministic, explainable risk
> scoring over community reports + verification. No medical diagnosis, no
> epidemiological inference engine in v1.**

## Stack

| Layer | Technology | Role |
| ----- | ---------- | ---- |
| Frontend | Mobile-first web app (Next.js / React); rapid prototype via Lovable | Citizen app + org dashboard |
| API | Supabase (PostgREST + Edge Functions) | Report/verify/score/alerts |
| UI | Tailwind + shadcn/ui (or Lovable-generated) | Product UI |
| Client data | TanStack Query | Server state |
| Auth | **Supabase Auth** (email/phone; anonymous reporting supported) | Sessions / identity |
| Database | **Supabase Postgres** + PostGIS | Reports, verifications, areas, risk scores, orgs, alerts |
| Maps | **Mapbox or Google Maps** | Neighborhood map + area overlays |
| Files | Supabase Storage | Report photos |
| Real-time | Supabase Realtime | Live report + alert updates |
| Risk engine | SQL views + Edge Functions (deterministic) | Volume, cluster, verification, signal mix, baseline |
| Hosting | Vercel + Supabase | Hackathon deploy |

## System Boundaries

- `src/app/` — citizen app routes: landing, home (your area), report, map,
  alerts, profile
- `src/app/(org)/` — organization dashboard routes: overview, hotspots, reports,
  trends, settings
- `src/server/api/` — edge functions / RPC for report, verify, risk score
- `src/server/risk/` — risk-score engine (pure functions + SQL)
- `supabase/` — migrations, seed (baseline areas), storage buckets, RLS policies
- `context/` + `docs/` — product ground truth
- `.cursor/skills/` — agent skills (no app build yet)

## Storage Model

- **Postgres:** users (Supabase Auth), profiles, reports, verifications, areas
  (townships/wards with PostGIS geometry + baseline), risk_scores (snapshot per
  area per compute), organizations, org_subscriptions, alerts, report_photos
- **Geospatial:** `geometry(Point)` on reports, `geometry(Polygon)` on areas —
  enables 1 km clustering, within-area aggregation, "near me" queries
- **Baseline:** per-area historical report rates so current activity can be
  compared to normal

## Auth and Access Model

- **Supabase Auth** email/password; phone optional; **anonymous reporting** =
  report row with `user_id IS NULL`
- **Citizen role:** create reports, verify/dispute, receive alerts, view risk
- **Organization role:** read aggregated risk + underlying reports for
  subscribed areas; no identity data beyond report metadata
- **RLS:** reports readable (aggregated) publicly; PII/identity columns scoped to
  owner; org data scoped to org subscription
- Reports are **signals, not diagnoses** — no health data fields beyond
  "illness cluster" category

## Risk engine (non-LLM core)

Deterministic, explainable WASH Risk Score per area (0–100):

- **Volume vs baseline** — recent report count vs the area's historical normal
- **Cluster density** — reports concentrated within ~1 km
- **Verification confidence** — independent confirms vs disputes
- **Signal mix** — water + sanitation + flooding + illness combinations weigh
  more than single-type reports
- **Recency** — exponential decay so old reports fade

Output includes a per-component breakdown so every score can answer *"why did
this change?"*

## System Design & Infrastructure

| Concept | Service / Tech | Notes |
|---------|---------------|-------|
| **Compute** | Next.js on Vercel + Supabase Edge Functions | Serverless |
| **Database** | Supabase Postgres + PostGIS | Reports + geospatial + scores |
| **Maps** | Mapbox / Google Maps | Area overlays + markers |
| **Auth** | Supabase Auth | Email/phone; anonymous option |
| **Storage** | Supabase Storage | Report photos |
| **Real-time** | Supabase Realtime | Live alerts/reports |
| **Rate limiting** | Per-user report/verify limits | Abuse control |
| **Observability** | Supabase logs + Vercel analytics | Later: Sentry |

## Scaling & Performance Constraints

- Pilot: hundreds to low thousands of users, 2–3 townships
- Report insert latency: near-real-time (Realtime push to map/alerts)
- Risk score refresh: on-write incremental or scheduled (e.g. every 15 min per
  area)
- Data volume: small for MVP (thousands of reports) — plain indexed queries +
  a few PostGIS functions

## Invariants

1. Reports are **signals, not diagnoses** — never claim an outbreak/diagnosis.
2. Risk scores are transparent and explainable (component breakdown).
3. Anonymous reporting must always be possible.
4. PII is minimized; identity/contact data never exposed to organizations.
5. Verification + clustering gate outlier reports (duplicate/misinformation
   handling).
6. No secrets in git.
7. **Do not scaffold/build the app until product owner says build** — context +
   specs first; MVP vertical waits for explicit **build**.

## MVP Vertical (when build starts)

`report (anonymous or signed-in) → appears on map → nearby user verifies →
risk score updates → citizen alert / org dashboard view`

Version 1 is five things only: report, map, verify, basic risk score, two views.