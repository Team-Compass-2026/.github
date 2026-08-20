# Domain Model — WaterWatch (MVP)

**Team Compass🧭 · Active build · Main app: Prisma 7 + Neon (see `waterwatch/prisma/schema.prisma`) · Lovable path: Supabase Auth + PostGIS**

## Entities

User (Supabase Auth) · Profile · Report · Verification · Area (township/ward,
PostGIS geometry) · RiskScore · Organization · OrgSubscription · Alert · Photo

Computed (not SoT): RiskScore breakdown, verification confidence, area trends.

## Relationships

User 0..1 Profile · User 0..* Report (anonymous: user_id NULL) ·
Report 1..* Verification — User · Report *..1 Area ·
Area 1..* RiskScore (snapshot per compute) ·
Organization 1..* OrgSubscription — Area · Area 1..* Alert

## Bounded contexts

auth · reporting · verification · geospatial · risk-engine · alerts ·
organization-intelligence

## Invariants

RLS on all tables · anonymous reporting always possible · reports are signals,
not diagnoses · independent-user cap per verification · no PII exposure to orgs ·
score always has a component breakdown · rate-limited submissions

Full write-up: enterprise domain-model phase (pivot 2026-08-20).