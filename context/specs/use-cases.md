# Use Cases — WaterWatch (MVP)

**Team Compass🧭 · Supabase Auth · No build until requested**

| ID | Name | Primary actor |
|----|------|----------------|
| UC-1 | Seed pilot townships + baselines | Admin |
| UC-2 | Report a WASH problem (anonymous or signed-in) | Resident |
| UC-3 | View neighborhood map + risk areas | Resident |
| UC-4 | Verify / dispute a nearby report | Resident |
| UC-5 | Receive localized alerts | Resident |
| UC-6 | View area risk explanation | Resident |
| UC-7 | View org dashboard (hotspots + drill-down) | Organization |
| UC-8 | Manage org subscription/filters | Organization |

**Demo:** UC-2 → UC-3 → UC-4 → UC-5 → UC-7 (UC-1 before demo).

## Domain (sketch)

User (Supabase Auth) 0..* Report (anonymous: user_id NULL) ·
Report 1..* Verification — User · Report *..1 Area · Area 1..* RiskScore ·
Area 1..* Alert · Organization 1..* OrgSubscription — Area

## Architecture

- RLS on all tables · anonymous report path (user_id NULL) · risk-score
  functions in SQL/edge functions · Realtime push for maps/alerts ·
  signals-not-diagnoses

Full architect write-up: enterprise phase use-cases (pivot 2026-08-20).