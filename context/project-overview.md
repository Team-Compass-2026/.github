# WaterWatch — Project Overview

**Team:** Team Compass 🧭 · **Hackathon:** DEEP · **Product:** WaterWatch

> **Brand:** WaterWatch · Primary tagline: *See the risk. Share the signal.
> Protect the community.* · Short: *Myanmar's community WASH intelligence
> layer.*
> Descriptor: *Turning community observations into early warnings for waterborne-disease risk*
> Brand mark: **WATERWATCH**
>
> Canonical full spec: `context/product-spec.md`. Prototype development brief:
> `context/prototype-spec.md`. Implementation specs: `context/specs/`.

---

## The Problem

Myanmar faces recurring challenges involving unsafe water, sanitation, flooding,
and infectious disease outbreaks. This is not simply a problem of people lacking
health knowledge. It is also a **problem of information and response**:

- Water and sanitation problems can emerge at the neighborhood level before they
  become visible in formal health statistics.
- Residents may know that their local water looks contaminated, a drain has
  overflowed, or sewage is leaking, but there is no simple way to turn these
  observations into a structured community warning.
- Public-health organizations and NGOs need localized information to decide
  **where to investigate and where to prioritize limited resources**.
- Communities often receive information after a problem has already become
  serious.

The fundamental problem is not *"communities lack information about water"* but:

> **"There is no efficient bridge between what residents observe about local
> water and sanitation and what organizations need to know to respond."**

**Key statistics:**
- 3,421 hospitalized acute watery diarrhea (AWD) cases in Yangon Region between
  24 June and 25 August 2024, including 160 severe-dehydration cases. — WHO
- After 25 August 2024, no further official Yangon AWD data were shared
  publicly, while open-source information suggested cases were increasing in
  some townships. — WHO
- 8.9 million people in Myanmar need critical WASH services. — UNICEF
- Over 40% of households lack safely managed drinking water; nearly 40% lack
  safely managed sanitation; one in three lack basic hygiene services. — UNICEF

## The Gap

**We have people who observe problems.**
**We have organizations that need information.**
**But we lack an efficient bridge between the two.**

## Root Causes

- Water and sanitation signals emerge at the neighborhood level before they show
  up in formal health statistics.
- No simple, low-friction channel for residents to turn observations into
  structured warnings.
- Official information can be delayed or limited (e.g. Yangon AWD reporting gap
  after August 2024).
- Organizations lack localized data to prioritize limited resources.
- Communities receive information only after a problem has become serious.

## Jobs-to-be-Done

- When I see dirty or cloudy water, I want to **report it quickly** so that my
  community and responders know about it.
- When I want to know if my neighborhood is safe, I want to **see local WASH
  risk** so that I can decide what precautions to take.
- When someone reports a problem near me, I want to **verify or dispute it** so
  that misinformation does not become an outbreak signal.
- When I live in an area with repeated reports, I want to **receive local
  alerts** so that I can act before the situation worsens.
- When my organization responds to WASH issues, I want **location-based risk
  intelligence** so that we can prioritize where to investigate first.

## Our Solution

WaterWatch is a **community-powered WASH early-warning platform**. Citizens
report local water and sanitation problems; WaterWatch combines community
reports, environmental information, geographic data, and historical patterns to
generate **neighborhood-level WASH Risk Scores** and localized alerts.

The platform does **not** diagnose cholera. Instead, it identifies **unusual
community-level signals that may warrant attention**.

**Core loop:** Observe → Report → Verify → Analyze → Alert → Prioritize

**Master flow:** Residents observe → submit structured report (what / where /
when / photo, anonymous option) → nearby users verify → system aggregates
geographically and temporally → citizens receive localized alerts → organizations
receive a prioritization dashboard.

## How It Is Different From Other Solutions

A resident's observation of brown water is, by itself, a small signal. A health
ministry's dashboard is, by itself, too slow and too coarse. WaterWatch is the
only piece that **connects resident observations → structured warnings →
verification → neighborhood risk → local alerts → prioritized response** into
one loop.

Differentiation: **community participation + geographic aggregation + signal
verification + information reciprocity** — not a survey tool, not a government
hotline, not a clinical tracker.

## How It Works: User Journey

1. **Observe** — a resident notices dirty water, sewage overflow, flooding,
   broken infrastructure, unsafe sanitation, or unusual illness.
2. **Report** — submit what happened, where, when, and (optionally) a photo;
   anonymous reporting supported.
3. **Verify** — nearby users confirm or dispute; independent confirmations raise
   confidence.
4. **Analyze** — the system looks for unusual increases, geographic clusters,
   repeated reports, signal combinations, and changes vs. historical patterns.
5. **Alert** — citizens receive localized alerts with practical
   recommendations.
6. **Prioritize** — organizations receive a dashboard of priority zones and
   underlying reports.

## Unique Selling Point

WaterWatch gives every user something valuable in return for their
participation. Citizens contribute information and receive **better information
about their own neighborhood** — local alerts, risk scores, verification, and
practical recommendations. Organizations receive **where to investigate first**.

> See the risk. Share the signal. Protect the community.

## Impacts

- Earlier detection of WASH-related risk in neighborhoods
- Better targeting of limited response resources
- Reduced information asymmetry between communities and responders
- Community participation in health monitoring
- Increased WASH awareness and preparedness
- A replicable early-warning layer for other cities and other
  environmentally-linked health risks

## Business Model

**Primary revenue — WASH Intelligence Platform:**
- Free citizen platform (maximize the network): report, view risk, alerts,
  verify, hotspots, prevention info.
- Paid organizational platform: hotspot map, trends, risk scoring, analytics,
  geographic filtering, automated reports, export/API tiers.

**Secondary revenue — Sponsored WASH Monitoring ("WASH Monitoring as a
Service"):** an NGO funds monitoring of specific townships for a period
($15,000–50,000/year depending on scale). Selling an outcome/service, not
software.

## Market Entry Strategies

- **Phase 1 — One Yangon pilot:** 2–3 townships, partners (universities, student
  orgs, NGOs, community groups, clinics, water-testing providers), 500–1,000
  users.
- **Phase 2 — Build the data network:** "Check Your Neighborhood" campaigns,
  WaterWatch Guardians.
- **Phase 3 — Sell the intelligence:** 30-day pilot dashboards → subscriptions.
- **Phase 4 — Expand:** Yangon → Mandalay → other Myanmar cities → regional WASH
  markets.

## The Ask

We are seeking **US$10,000 in pilot funding, technical support, and
partnerships** to build and test WaterWatch in Yangon. The pilot answers three
questions:

1. Will people actually report WASH problems?
2. Can community reports produce useful localized risk signals?
3. Will organizations pay for the resulting intelligence?

## Team

**Team Compass 🧭**
- Product: WaterWatch
- Hackathon: DEEP 2026

## MVP (Must) — Version 1, five things only

1. User reports a WASH problem.
2. Report appears on a map.
3. Nearby users can verify it.
4. System calculates a basic risk score.
5. Users and organizations receive different views of the information.

## Later (out of MVP build)

Sensor/rainfall data feeds · automated intelligence reports · export/API access
· multi-language · offline-first reporting · contribution badges/rewards ·
partner rewards marketplace · multi-city expansion · sponsored monitoring
programs.

## Target Users

**Primary — citizens:** Yangon residents, families in flood/sanitation-vulnerable
areas, students and young adults, community volunteers, residents dependent on
local water sources or vendors.

**Secondary — organizations:** NGOs, humanitarian and WASH organizations,
clinics and health facilities, researchers, water-service providers, local
authorities.

## Ethics & Privacy

Reports are **signals, not diagnoses**. Anonymous reporting fully supported;
identity optional; PII minimized. Verification + clustering reduce
misinformation. The platform informs communities — it does not surveil them.
Community data is not resold in ways that harm communities.

## Success Metrics

- **User:** reports submitted, active reporters per township, verification
  completion rate, alert opt-in, weekly active users
- **Signal quality:** verified-report rate, duplicate rate, agreement with
  on-the-ground checks
- **Outcome:** observation→alert time, organization engagement, pilot
  subscription conversions
- **Pilot questions:** Will people report? Do signals align with reality? Will
  organizations pay?

---

## Reference: Team Compass (Heritage)

*The original pitch framing (kept as reference — the brand is now WaterWatch).*

The previous project was **Career GPS** — an AI-powered career navigation
platform helping young people turn fragmented career information into a
personalized, evidence-based roadmap. Brand: *Stop guessing. Start building your
career.* Journey: **Confusion → Understanding → Planning → Learning → Action →
Career Readiness**.

Team Compass 🧭 retains its name; the product is now **WaterWatch**.