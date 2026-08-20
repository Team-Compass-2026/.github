# Spec: WaterWatch MVP pillars

## Goal

Report (anonymous + signed-in) → map → verify → basic risk score → citizen
alert / org dashboard — the five things only, end-to-end. **Implemented in the
main app** (Next.js + Neon + Better Auth + Hono); mirrored on the Lovable/
Supabase path.

## In scope

- Neon schema + Prisma 7 + seed (main app) · Supabase schema + RLS + PostGIS (Lovable)
- Report form: type, location (map pin / GPS), time, photo (optional),
  anonymous option
- Report appears on a map with report-type markers
- Nearby users verify (confirm/dispute) with per-report independent-user cap
- Basic risk score per area with component breakdown
- Citizen alerts (localized) + organization dashboard (hotspots + drill-down)
- Seed 2–3 pilot townships with baseline report rates

## Out of scope

- Sensors/rainfall feeds, multi-city, partner rewards, multi-language,
  export/API tiers

## Acceptance (when built)

1. Anonymous report flows end-to-end (report → map → verifiable).
2. Unauthenticated writes rejected (RLS).
3. Risk score explains its components; stale areas decay to LOW.
4. Org dashboard shows hotspots + underlying reports; identity fields never
   exposed.

## Skills to load when building

- Supabase / PostGIS / RLS
- Mapbox or Google Maps integration
- Risk-engine pure functions