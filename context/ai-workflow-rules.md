# AI Workflow Rules — WaterWatch

## Approach

Spec-driven against six-file context + `docs/product/`. Do not invent report
categories, townships, or scoring rules outside the curated product design.

**Current mandate: improve docs and skills only — do not build/scaffold the app
until the user explicitly asks.**

## Scoping Rules

- One MVP pillar per implementation cycle when build starts
- Load `.cursor/skills/` for Supabase/PostGIS/maps/risk as available
- Auth is Supabase Auth only; anonymous reporting is a first-class path

## When to Split Work

Split if combining: report intake+map, verification+risk score, citizen app+org
dashboard.

## System Design Triggers

| Trigger | Doc / skill |
|---------|-------------|
| Reports / verifications | `architecture.md` storage + RLS |
| Risk score / alerts | `architecture.md` risk engine |
| Map / geospatial | PostGIS + Mapbox/Google Maps |
| New report types / areas | `product-spec.md` §6 + `data/README.md` |

## Verification (when building)

- Demo path: report → map → verify → risk score → citizen alert / org view
- Anonymous report works end-to-end
- Unauthenticated writes rejected (RLS)
- Risk score exposes a component breakdown
- Update `progress-tracker.md`

## Delivery Approach

1. Finish enterprise stories/acceptance (now)
2. Optional sample data (report types, townships, baseline)
3. Scaffold only on explicit build request
4. P0 vertical: report → map → verify → risk score → alerts/dashboard