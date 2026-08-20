# Tech Selection — WaterWatch (MVP)

**Team Compass🧭 · No build until requested**

| Decision | Choice |
|----------|--------|
| Database | **Supabase** (Postgres + PostGIS) |
| Auth | **Supabase Auth** (email/phone; anonymous reporting) |
| Frontend | Mobile-first web (Next.js/React); rapid prototype via **Lovable** |
| Maps | **Mapbox** or **Google Maps** |
| Files | Supabase Storage (report photos) |
| Real-time | Supabase Realtime (live reports/alerts) |
| Host | Vercel |
| Package manager | Bun 1.3 |
| Risk engine | SQL views + edge functions (deterministic, explainable) |

## Env names
`NEXT_PUBLIC_SUPABASE_URL` · `NEXT_PUBLIC_SUPABASE_ANON_KEY` ·
`SUPABASE_SERVICE_ROLE_KEY` · `NEXT_PUBLIC_APP_URL` · map provider key
(`NEXT_PUBLIC_MAPBOX_TOKEN` or Google Maps key) · optional n8n/Telegram vars

Full rationale: enterprise tech-selection (pivot 2026-08-20).