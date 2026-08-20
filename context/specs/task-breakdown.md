# Task Breakdown — WaterWatch (MVP)

**Team Compass🧭 · Estimates S/M/L · Depends-on listed**

## M1 Supabase shell + data model
- T1.1 Scaffold mobile-first app + env stubs — **M**
- T1.2 Supabase project + PostGIS + tables + RLS (reports, verifications,
  areas, risk_scores, orgs, alerts) — **L** ← T1.1
- T1.3 Seed 2–3 pilot townships + baseline report rates (US-1) — **S** ← T1.2
- T1.4 Auth (email/phone) + anonymous report path — **M** ← T1.2

## M2 Report + map
- T2.1 Report form (type, location, time, photo, anonymous) (US-2) — **M** ← T1.4
- T2.2 Report insert → map marker + Realtime push (US-3) — **M** ← T2.1
- T2.3 Map with area overlays + area detail sheet — **L** ← T2.2

## M3 Verification
- T3.1 Verify/confirm-dispute endpoint + UI (US-4) — **M** ← T2.2
- T3.2 Independent-user cap + confidence aggregation — **S** ← T3.1

## M4 Risk score + alerts
- T4.1 Risk-score function (volume/cluster/verification/signal mix/recency)
  (US-5) — **M** ← T3.2, T1.3
- T4.2 Component breakdown + "See why" UI — **S** ← T4.1
- T4.3 Localized citizen alerts (US-6) — **M** ← T4.2

## M5 Org dashboard + demo
- T5.1 Org hotspot list + drill-down to reports (US-7) — **M** ← T4.1
- T5.2 Filters (date, type, township) + trend indicators — **M** ← T5.1
- T5.3 Full demo rehearsal (report → verify → score → alert → dashboard) — **M**
  ← T4.3, T5.2
- T5.4 Vercel + Supabase deploy — **S** ← T5.3

Start at **T1.1** only after explicit **build**.