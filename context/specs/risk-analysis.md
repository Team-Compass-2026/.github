# Risk Analysis — WaterWatch (MVP)

**Team Compass🧭 · Active build · Main app: Better Auth session + Hono rate limits · Lovable path: Supabase Auth + RLS**

## P0
- RLS misconfiguration → identity/report leakage (policies on every table;
  org views exclude identity fields)
- Spam / duplicate / fake reports inflate scores (cluster + verification gates,
  rate limits, independent-user cap)
- Anonymous path accidentally blocked (report must work with user_id NULL)

## P1
- Risk-score tuning (thresholds) · PostGIS query cost · storage/photo abuse ·
  alert fatigue
- Misinformation damaging community trust (signals-not-diagnoses copy +
  explainable scores)

## P2
- Scope creep (multi-city, sensors, partner rewards) · n8n token leakage
  (secrets already gitignored)

## Mitigation themes
RLS-first schema · rate limits · verification weighting · explainable scores ·
anonymous reporting always on · pilot 2–3 townships before scaling

Full table: enterprise risk-analysis phase (pivot 2026-08-20).