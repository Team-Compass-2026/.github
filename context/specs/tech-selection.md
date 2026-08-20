# Tech Selection — WaterWatch (MVP)

**Team Compass🧭 · Active development**

## Locked choice (main app, this repo)

| Layer | Choice |
|-------|--------|
| Framework | **Next.js 16** (root `app/`, no `src/`) + TypeScript |
| Database | **Neon Postgres** via **Prisma 7** (`@prisma/adapter-pg`) |
| Auth | **Better Auth** (email/password, cookie sessions) |
| API | **Hono** (catch-all route) + typed client |
| Client data | **TanStack Query** |
| Maps | **React Leaflet** + OpenStreetMap (free, no API key) |
| Edge logic | Next 16 built-in **`proxy.ts`** (security headers + API CORS) |
| Risk engine | `lib/risk.ts` (deterministic, explainable) |
| Host | Vercel |
| Package manager | Bun 1.3 |

## Prototype path (Lovable + Supabase)

| Layer | Choice |
|-------|--------|
| Database | **Supabase** (Postgres + PostGIS) |
| Auth | **Supabase Auth** (email/phone; anonymous reporting) |
| Maps | **Mapbox** or **Google Maps** |
| Files | Supabase Storage (report photos) |
| Real-time | Supabase Realtime (live reports/alerts) |
| Risk engine | SQL views + edge functions (deterministic, explainable) |

## Env names (main app)

`DATABASE_URL` (Neon) · `BETTER_AUTH_SECRET` · `BETTER_AUTH_URL` ·
`BETTER_AUTH_TRUSTED_ORIGINS` · `API_ALLOWED_ORIGINS` (optional, proxy CORS)

See `waterwatch/.env.example` and `waterwatch/docs/setup.md`.

Full rationale: enterprise tech-selection (pivot 2026-08-20, dual-path decision).