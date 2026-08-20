# Spec: WaterWatch MVP pillars (docs-ready; build later)

## Goal

When build starts: report (anonymous + signed-in) → map → verify → basic risk
score → citizen alert / org dashboard — the five things only, end-to-end.

## In scope (first build)

- Supabase project + schema + RLS + PostGIS setup
- Report form: type, location (map pin / GPS), time, photo (optional),
  anonymous option
- Report appears on a map with report-type markers
- Nearby users verify (confirm/dispute) with per-report independent-user cap
- Basic risk score per area with component breakdown
- Citizen alerts (localized) + organization dashboard (hotspots + drill-down)
- Seed 2–3 pilot townships with baseline report rates

## Out of scope

- Scaffold before explicit "build" request
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