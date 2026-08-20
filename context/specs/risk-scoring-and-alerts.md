# Spec: Risk scoring + localized alerts (MVP slice)

## Goal

Given verified community reports, compute an explainable WASH Risk Score per
area and surface it to citizens (local alerts) and organizations (hotspot
priority).

## In scope

- Risk-score function (deterministic, non-LLM):
  volume vs baseline · cluster density (~1 km) · verification confidence ·
  signal mix (water + sewage + flooding + illness) · recency decay
- Per-component breakdown so each score explains *why it changed*
- Score snapshot per area on a schedule (e.g. every 15 min) + on-write refresh
- Citizen alert: reports within 1 km of user → localized warning with practical
  recommendation
- Org view: hotspot list (township × score × trend) with drill-down to reports

## Out of scope

- Medical diagnosis / outbreak declaration
- Sensor/rainfall feeds (future)
- Complex epidemiological modeling

## Acceptance

1. A seeded area with 3× baseline reports yields HIGH score with a breakdown
   naming volume/cluster/verification/signal mix.
2. Old reports decay — a stale area with no recent reports returns to LOW.
3. Confirmed reports raise confidence more than unconfirmed ones.
4. Alerts fire only within the configured radius of a user's area.
5. Every score card explains its components (no unexplained numbers).

## Risks

- Spam/duplicate reports inflate scores → cluster + verification gates
- Gaming via fake verifications → independent-user cap per report
- Threshold tuning → validate against pilot townships before launch