# AI Workflow Rules — WaterWatch

## Approach

Spec-driven against six-file context (`context/*`) + `waterwatch/docs/`. Do not
invent report categories, townships, or scoring rules outside the curated
product design.

**Current mandate: active development on the main app (Next.js + Neon). Keep the
Lovable/Supabase prototype path in sync via `waterwatch/docs/lovable/` prompts.**

## Scoping Rules

- One MVP pillar per implementation cycle
- Load `.cursor/skills/` for Supabase/PostGIS/maps/risk as available
- Main app auth is **Better Auth**; the Lovable path uses **Supabase Auth**.
  Anonymous reporting is a first-class path on both.

## When to Split Work

Split if combining: report intake+map, verification+risk score, citizen app+org
dashboard.

## System Design Triggers

| Trigger | Doc / skill |
|---------|-------------|
| Reports / verifications | `architecture.md` storage + access control |
| Risk score / alerts | `architecture.md` risk engine |
| Map / geospatial | Main app: React Leaflet + OSM (haversine in risk engine) · Lovable path: PostGIS + Mapbox/Google Maps |
| New report types / areas | `context/product-spec.md` §6 + `context/specs/` |

## Verification (when building)

- Demo path: report → map → verify → risk score → citizen alert / org view
- Anonymous report works end-to-end
- Unauthenticated writes rejected (auth session required; RLS on Lovable path)
- Risk score exposes a component breakdown
- Update `progress-tracker.md`

## Delivery Approach

1. One MVP pillar per cycle (report intake+map, verification+risk score,
   citizen app+org dashboard)
2. Seed sample data (report types, townships, baseline)
3. P0 vertical: report → map → verify → risk score → alerts/dashboard
4. Gate each pillar with `bunx tsc --noEmit`, `bun run lint`, `bun run build`