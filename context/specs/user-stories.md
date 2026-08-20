# User Stories & Acceptance — WaterWatch

**Team Compass🧭 · Active build · Main app: Prisma 7 + Neon + Better Auth · Lovable path: Supabase Auth · MVP five things**

## Stories

| ID | Title | Priority | SP |
|----|-------|----------|-----|
| US-1 | Seed pilot townships + baseline rates | Must | 3 |
| US-2 | Report a WASH problem (types, location, photo, anonymous) | Must | 8 |
| US-3 | Report appears on neighborhood map | Must | 5 |
| US-4 | Verify / dispute nearby reports | Must | 5 |
| US-5 | Basic risk score per area + explanation | Must | 8 |
| US-6 | Localized citizen alerts | Must | 5 |
| US-7 | Organization dashboard (hotspots + drill-down) | Must | 8 |

Build order when requested: US-1 → US-2 → US-3 → US-4 → US-5 → US-6 → US-7

## Demo gate

Report (anonymous) → appears on map → neighbor verifies → risk score updates
with explanation → citizen alert fires → org dashboard shows the hotspot with
underlying reports. Reports are labeled signals, not diagnoses; identity fields
never exposed.

Full AC detail produced in enterprise PM phase (pivot 2026-08-20).