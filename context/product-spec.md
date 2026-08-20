# WaterWatch💧 — Master Project Context, Scope, Data & Product Specification

Canonical source of truth for the WaterWatch product. Distilled operational
view: `context/project-overview.md`. Specs that constrain implementation live
in `context/specs/`.

---

# 1. Project Identity

**Product name:** WaterWatch

**Team:** Team Compass 🧭

**Category:** Community-powered public-health early warning, WASH (Water,
Sanitation and Hygiene) monitoring, civic technology, geographic risk
intelligence, mobile-first reporting.

**Hackathon:** DEEP Hackathon 2026

**Core concept:** A community-powered WASH early-warning platform that lets
citizens report local water and sanitation problems and transforms those
observations into useful, location-based risk intelligence for waterborne-disease
prevention.

**Core metaphor:** Residents are the sensors of the neighborhood. Their daily
observations — dirty water, sewage overflow, flooding, broken infrastructure,
unusual illness — are signals that, combined and analyzed geographically and
temporally, can reveal patterns before they become crises.

**Core promise:** *See the risk. Share the signal. Protect the community.*

**Brand descriptor:** *Turning community observations into early warnings for waterborne-disease risk*

**Brand mark:** WATERWATCH (stylized/hero contexts)

**Positioning:** *Myanmar's community WASH intelligence layer.*

**Brand idea:** *We are the information bridge between people who observe
problems and organizations that need information.*

---

# 2. The Problem

Myanmar faces recurring challenges involving unsafe water, sanitation, flooding,
and infectious disease outbreaks.

This is not simply a problem of people lacking health knowledge. It is also a
**problem of information and response**:

- Water and sanitation problems can emerge at the neighborhood level before they
  become visible in formal health statistics.
- Residents may know that their local water looks contaminated, a drain has
  overflowed, or sewage is leaking, but there is no simple way to turn these
  observations into a structured community warning.
- Public-health organizations and NGOs need localized information to decide
  **where to investigate and where to prioritize limited resources**.
- Communities often receive information after a problem has already become
  serious.

### The scale of the problem

Yangon's **2024 acute watery diarrhea (AWD) outbreak** is a concrete example.
WHO reported **3,421 hospitalized AWD cases in Yangon Region between 24 June and
25 August 2024**, including **160 cases with severe dehydration**. More than 400
hospitalized cases were reported each week from epidemiological week 31 onward.
([World Health Organization](https://www.who.int/southeastasia/internal-publications-detail/mawdcoesr00322092024))

WHO's reports also demonstrate that official information can have limitations:
after 25 August 2024, WHO reported that no further official Yangon AWD data were
being shared publicly, while open-source information suggested cases were
increasing in some townships.
([World Health Organization](https://www.who.int/southeastasia/internal-publications-detail/mawdcoesr00425092024))

The underlying WASH problem is broader than cholera. UNICEF Myanmar's current
WASH assessment states that **8.9 million people in Myanmar need critical WASH
services**; over **40% of households lack safely managed drinking water**, nearly
**40% lack safely managed sanitation**, and **one in three households lack basic
hygiene services**. Flooding and other disasters can contaminate water sources
and increase the risk of AWD and cholera.
([UNICEF](https://www.unicef.org/myanmar/water-sanitation-and-hygiene-wash))

---

# 3. The Gap

**We have people who observe problems.**
**We have organizations that need information.**
**But we lack an efficient bridge between the two.**

---

# 4. Target Users

## Primary users — Citizens

Especially:

- Yangon residents
- Families in areas vulnerable to flooding or sanitation problems
- Students and young adults
- Community volunteers
- Residents who depend on local water sources or vendors

They want to know:

> **"Is my neighborhood currently experiencing a water or sanitation problem?"**

## Secondary users — Organizations

Organizations that can use aggregated WaterWatch intelligence:

- NGOs
- Humanitarian organizations
- WASH organizations
- Clinics and health facilities
- Researchers
- Water-service providers
- Local authorities

Their question is:

> **"Where should we investigate or intervene first?"**

---

# 5. The Solution

## WaterWatch

A **community-powered WASH early-warning platform** that allows citizens to
report local water and sanitation problems and transforms those reports into
useful, location-based risk intelligence.

WaterWatch combines:

**Community reports + environmental information + geographic data + historical
patterns**

to generate:

### A neighborhood-level WASH Risk Score

For example:

## Hlaing Tharyar

> **WASH Risk: HIGH — 82/100**
>
> 23 water-quality reports
> 8 sewage incidents
> Recent flooding
> Increased community-reported diarrhea
> Limited nearby verified safe-water sources

The platform does **not diagnose cholera**. Instead, it identifies **unusual
community-level signals that may warrant attention**.

---

# 6. How WaterWatch Works

### Step 1 — Observe

A resident notices:

- Dirty/cloudy water
- Sewage overflow
- Flooding
- Broken water infrastructure
- Unsafe public sanitation
- Unusual increases in diarrhea within their household/community

### Step 2 — Report

The user opens WaterWatch and submits:

**What happened?**
**Where?**
**When?**
**Photo, if available**

The report can be submitted **anonymously**.

### Step 3 — Verify

Nearby users can confirm or dispute observations. For example:

> "Brown water reported at this location."

Nearby users receive:

> "Can you verify this?"

If several independent users report the same phenomenon, confidence increases.
This reduces the risk of individual misinformation becoming an outbreak signal.

### Step 4 — Analyze

WaterWatch aggregates reports geographically and temporally. The system looks
for:

- unusual increases in reports
- geographic clusters
- repeated reports from the same location
- combinations of water + sanitation + flooding signals
- changes compared with historical patterns

### Step 5 — Alert

Citizens receive localized information:

> **WaterWatch Alert**
>
> Multiple water-quality concerns have been reported within 1 km of your
> location. Consider using treated/boiled drinking water until the situation is
> clarified.

### Step 6 — Prioritize

Organizations receive a more detailed dashboard:

> **Priority Zone: Township X**
>
> Risk: 87/100
> Trend: ↑ 41%
> Water reports: 37
> Sanitation reports: 12
> Community illness signals: ↑
> Flooding: Yes

They can then decide where to send:

- water-testing teams
- WASH workers
- hygiene supplies
- ORS
- safe-water resources
- public-health messaging

---

# 7. Why Would Citizens Participate?

This is critical to WaterWatch's success. We do **not** want the model to be:

> "Please volunteer your information for the greater good."

Instead:

> **"You contribute information, and in return you receive better information
> about your own neighborhood."**

### Citizen value proposition

Users receive:

1. **Local alerts** — know when unusual water/sanitation problems are appearing
   nearby.
2. **Neighborhood risk score** — understand the current WASH situation around
   them.
3. **Community verification** — see whether other residents are experiencing the
   same problem.
4. **Practical recommendations** — receive evidence-based actions appropriate to
   the situation.
5. **Contribution reputation** — useful, verified reports can earn community
   reputation/badges.
6. **Partner rewards — future stage** — verified contributions could eventually
   earn points redeemable for: water testing, water filters, safe-water
   services, hygiene products, partner discounts.

The most important incentive is **information reciprocity**.

---

# 8. Supporting Research

### Evidence 1 — Yangon has experienced substantial AWD outbreaks

WHO documented 3,421 hospitalized AWD cases in Yangon Region between June and
August 2024, with 160 severe-dehydration cases.
([World Health Organization](https://www.who.int/southeastasia/internal-publications-detail/mawdcoesr00322092024))
This demonstrates that the problem is not hypothetical.

### Evidence 2 — WASH vulnerabilities remain widespread

UNICEF Myanmar currently reports that:

- 8.9 million people need critical WASH services
- 40% of households lack safely managed drinking water
- nearly 40% lack safely managed sanitation
- one-third lack basic hygiene services

UNICEF also highlights flooding and disasters as factors that can contaminate
water sources and increase waterborne-disease risks.
([UNICEF](https://www.unicef.org/myanmar/water-sanitation-and-hygiene-wash))

### Evidence 3 — Early information matters

WHO's cholera response framework emphasizes surveillance, early detection,
community engagement and WASH interventions as important components of outbreak
prevention and response. This supports the basic premise that **earlier signals
can enable earlier action**.

### Evidence 4 — Digital WASH management is already viable

mWater demonstrates that organizations are willing to use digital platforms for
water and sanitation data collection, mapping, monitoring and decision-making.
It operates across 198 countries and territories and has been used by
governments, utilities, NGOs, researchers and community organizations.
([mWater](https://www.mwater.co/impact))

Therefore, WaterWatch isn't proposing that organizations suddenly start using
digital WASH intelligence. We're proposing a **new data source and user layer**
for that ecosystem.

---

# 9. The Product

## Citizen App

### Home

**Your area**
WASH Risk: 🟠 MODERATE
Recent reports: 8

### Report

**What did you observe?**
○ Unsafe water
○ Sewage
○ Flooding
○ Broken infrastructure
○ Sanitation problem
○ Illness cluster
○ Other
📍 Location
📷 Photo
**SUBMIT**

### Map

A live map showing:
🔴 High-risk areas
🟠 Moderate-risk areas
🟢 Low-risk areas
Users can tap an area to understand why its risk score has changed.

### Alerts

> **Elevated risk detected near you**
>
> Multiple residents have reported water-quality problems in your area.

## Organization Dashboard

This is the **monetizable product**.

### Yangon WASH Intelligence Dashboard

**Overall risk: 71/100**

| **Indicator**         | **Current** | **Trend** |
| --------------------- | ----------- | --------- |
| Water reports         | 247         | ↑ 38%     |
| Sanitation reports    | 84          | ↑ 61%     |
| Illness signals       | 129         | ↑ 72%     |
| Flood-related reports | 31          | ↑ 24%     |

### AI-generated priority areas

**1. Township A — HIGH**
**2. Township B — HIGH**
**3. Township C — MODERATE**

The organization can click a hotspot and investigate the underlying reports.

---

# 10. Business Model

## Primary Revenue: WASH Intelligence Platform

This is the **main business**. Organizations pay to access a professional
WaterWatch dashboard.

### Free citizen platform

Citizens get:

- Report problems
- View local WASH risks
- Receive alerts
- Verify reports
- See nearby hotspots
- Receive prevention information

**Price: Free** — this maximizes your network.

### Paid organizational platform

An NGO or humanitarian organization gets:

**WaterWatch Intelligence** (example dashboard)

> Yangon Region
> WASH Risk: **HIGH**

**Hotspots**

1. Township A — 87/100
2. Township B — 79/100
3. Township C — 73/100

**Signals**

- Water contamination reports ↑ 42%
- Sewage incidents ↑ 31%
- Flooding detected
- Illness reports ↑ 26%

And importantly:

> **"Where should we investigate first?"**

That's what they're paying for.

### What they receive

- Real-time hotspot map
- Historical trends
- Risk scoring
- Community-report analytics
- Geographic filtering
- Automated reports
- Alerts
- Organization-specific dashboards
- Export/API access at higher tiers

## Secondary Revenue: Sponsored WASH Monitoring

Instead of an NGO simply buying software, they can say:

> "We want WaterWatch to monitor 5 townships for us for 12 months."

They fund the entire monitoring program. For example:

**WaterWatch × NGO X — Yangon WASH Monitoring Program**
- Duration: 12 months
- Coverage: 5 townships
- Community users: 10,000+
- Water-risk monitoring
- Sanitation monitoring
- Community alerts
- Monthly intelligence reports

**NGO pays: $15,000–50,000/year** depending on scale.

WaterWatch uses the money to:

- recruit community users
- operate the platform
- train community monitors
- conduct verification
- maintain servers
- perform analysis
- produce reports

This is essentially **"WASH Monitoring as a Service."** It is much easier to
justify to an NGO than: "Please pay us $5,000 for access to our app." You're
selling an outcome/service, not software.

---

# 11. Viability and Feasibility

### Why could people use it?

Because they receive useful information about their own neighborhood.

### Why would organizations pay?

Because better geographic intelligence can help them prioritize limited
resources.

### Why could it scale?

The core software can be replicated across: **Yangon → Mandalay → other Myanmar
cities → other WASH-vulnerable regions.**

### Why could it have network effects?

More users → more observations → better local intelligence → more useful
platform → more users.

WaterWatch does not require us to build a sophisticated epidemiological system
on day one.

---

# 12. Hackathon MVP

## Frontend

- Mobile/web interface
- Report form
- Map
- Risk dashboard
- Alerts

## Backend

- User accounts
- Geolocation
- Report database
- Timestamp
- Verification system

---

# 13. Prototype and Technology

### Frontend

**Lovable** — rapidly build the citizen application and organization dashboard.

### Database

**Supabase** — store:

- users
- reports
- locations
- verification
- risk scores
- organizations

### Maps

Mapbox or Google Maps.

### Version 1 — Five things only:

1. User reports a WASH problem.
2. Report appears on a map.
3. Nearby users can verify it.
4. System calculates a basic risk score.
5. Users and organizations receive different views of the information.

That is enough to demonstrate the concept.

---

# 14. The Ask

## We are seeking support to pilot WaterWatch in Yangon.

### Initial pilot budget: US$10,000

| **Area**                               | **Budget**  |
| -------------------------------------- | ----------- |
| MVP development & cloud infrastructure | $2,500      |
| Community pilot & recruitment          | $2,000      |
| Data/field validation                  | $1,500      |
| Water-testing partnerships             | $1,500      |
| User incentives                        | $1,000      |
| Security, privacy & maintenance        | $1,000      |
| Contingency                            | $500        |
| **Total**                              | **$10,000** |

The goal is not to spend $10,000 building a giant platform. The goal is to
answer three questions:

1. **Will people actually report WASH problems?**
2. **Can community reports produce useful localized risk signals?**
3. **Will organizations pay for the resulting intelligence?**

If the pilot validates these three assumptions, WaterWatch can move from a
hackathon prototype to a real social-impact technology venture.

---

# 15. Go-to-Market Strategy

## Phase 1 — One Yangon pilot

Select **2–3 townships** with relevant WASH/flooding challenges. Partner with:
universities, student organizations, local NGOs, community groups, clinics,
water-testing providers. Recruit the first **500–1,000 users**.

## Phase 2 — Build the data network

Run campaigns such as:

> **"Check Your Neighborhood"**

Encourage residents to submit observations. Use university students and
community volunteers as initial **WaterWatch Guardians**.

## Phase 3 — Sell the intelligence

Once enough data exists, approach NGOs and humanitarian organizations. Offer:

> **30-day pilot of WaterWatch Intelligence Dashboard**

Demonstrate: "Here are the hotspots we identified." Then convert successful
pilots into subscriptions.

## Phase 4 — Expand

Yangon → Mandalay → other Myanmar cities → regional WASH markets.

---

# 16. Final Pitch

> **Every outbreak leaves signals before it becomes a crisis.**
>
> A resident sees dirty water.
> Another sees sewage overflowing.
> Someone else notices flooding.
> A family notices several people becoming sick.
>
> Individually, these observations may mean very little.
> **Together, they can reveal a pattern.**
>
> WaterWatch turns those scattered community observations into localized,
> actionable early warnings.
>
> **Citizens get information about the place where they live. Organizations get
> intelligence about where they should act.**
>
> We don't wait for an outbreak to become visible.
> **We build the information layer that helps communities see the warning signs
> earlier.**
>
> **WaterWatch — See the risk. Share the signal. Protect the community.**

We are seeking **US$10,000 in pilot funding, technical support, and
partnerships** to build and test WaterWatch in Yangon.

---

# 17. Beyond Cholera

## Myanmar's community WASH intelligence layer

Not just cholera. The same infrastructure could monitor risks associated with:

- acute watery diarrhea
- flooding
- contaminated water
- sanitation failures
- infrastructure breakdown
- other environmentally linked health risks

The ultimate goal:

> **From reactive outbreak response to proactive community-level prevention.**

---

# 18. Data Strategy & Sources

Not dependent only on crowd reports. Combine:

- **Community-generated data:** reports (type, location, time, photo),
  verifications, reputation.
- **Environmental information:** flooding events, rainfall, water-quality
  measurements (future).
- **Geographic data:** townships, neighborhoods, wards, proximity to water
  sources, infrastructure layers.
- **Historical patterns:** baseline report rates per area so current activity can
  be compared to normal.

---

# 19. Potential Data Model

- **User:** user_id, name (optional), phone/anonymous handle, location, roles,
  reputation
- **Report:** report_id, type (unsafe_water, sewage, flooding,
  broken_infrastructure, sanitation_problem, illness_cluster, other),
  description, lat/lng, township, photo_url, status (open/verified/closed),
  created_at, user_id (nullable for anonymous)
- **Verification:** verification_id, report_id, user_id, verdict
  (confirm/dispute), created_at
- **RiskScore:** area_id, township, score (0–100), trend, signals jsonb,
  computed_at
- **Area / Township:** area_id, name, boundary (geo), baseline stats
- **Organization:** org_id, name, tier, subscription status
- **Alert:** alert_id, area_id, message, severity, created_at
- **Badge / Reputation (future):** user_id, badge, earned_at

---

# 20. Data Quality Principles

- **Verification-weighted:** multiple independent confirmations raise confidence;
  disputes lower it.
- **Signal, not diagnosis:** scores identify unusual community-level signals that
  may warrant attention — never a medical diagnosis.
- **Transparent scoring:** each area explains why its score changed (counts,
  trend, signal mix).
- **Anonymous by default:** reporting must not require identity.

---

# 21. Differentiation

Not a health-statistics portal, not a government hotline, not a generic survey
tool, and not a disease tracker. Differentiation is the bridge:

**Resident observations → structured community warnings → neighborhood risk
intelligence → prioritized response.**

The product focuses on the entire early-warning loop for WASH-related risk.

---

# 22. Unique Selling Proposition

> A community-powered early-warning platform that turns scattered local
> observations about water and sanitation into actionable, location-based risk
> intelligence.

Short: *See the risk. Share the signal. Protect the community.*

Alternative: *Your neighborhood's early-warning system for water and sanitation.*

---

# 23. Impact

**Reduce:** delayed detection of WASH problems, misallocation of response
resources, community exposure to contaminated water, information asymmetry
between communities and responders.

**Increase:** early detection, localized response, community participation,
WASH awareness, coordination between citizens and organizations.

---

# 24. Social Impact

Especially valuable for communities that are last to appear in official
statistics — informal settlements, flood-prone wards, communities dependent on
vendors or untreated sources. Long-term vision: a WASH intelligence layer that
covers every city that faces waterborne-disease risk.

---

# 25. Ethics, Safety & Privacy

- Reports are **signals, not diagnoses** — the platform never claims a cholera
  or disease outbreak.
- **Anonymous reporting** must be fully supported; identity is optional.
- **PII minimization** — collect only what is needed for verification and
  location.
- **Misinformation controls** — verification system, duplicate clustering,
  clearly labeled confidence.
- **No surveillance framing** — the product exists to inform communities, not
  to monitor them on behalf of authorities.
- **Data stewardship** — community data should not be resold in ways that harm
  communities.

---

# 26. Success Metrics

- **User:** reports submitted, active reporters per township, verification
  completion rate, alert opt-in rate, weekly active users
- **Signal quality:** verified-report rate, duplicate rate, correlation with
  on-the-ground checks
- **Outcome:** time from observation to alert, organization engagement with
  dashboards, pilot subscription conversions
- **Pilot questions:** Will people report? Do signals align with reality? Will
  organizations pay?

---

# 27. MVP Scope

Focus on the essentials.

**Must have (Version 1 — five things only):**
1. User reports a WASH problem.
2. Report appears on a map.
3. Nearby users can verify it.
4. System calculates a basic risk score.
5. Users and organizations receive different views of the information.

---

# 28. Nice-to-Have Features (post-MVP)

Water-quality sensor integration · flood/rainfall data feeds · automated weekly
intelligence reports · export/API access · multi-language (Myanmar/Burmese,
ethnic languages) · offline-first reporting · contribution badges/reputation ·
partner rewards marketplace · area subscription alerts · historical trend
analytics.

---

# 29. Out of Scope for Initial MVP

Clinical/medical diagnosis · formal epidemiology · emergency response dispatch ·
full citizen-government hotline integration · large social network · complex
survey tooling · enterprise analytics platform.

The MVP proves the core hypothesis:

> Community reports + verification + geographic aggregation can produce useful
> localized early warnings for WASH-related risk.

---

# 30. Validation Hypotheses

1. Residents will report WASH problems when they receive useful local
   information in return.
2. Community reports (verified) can produce localized risk signals that align
   with on-the-ground reality.
3. Organizations will pay for the resulting intelligence to prioritize limited
   resources.
4. Verification meaningfully reduces the risk of individual misinformation
   becoming an outbreak signal.

---

# 31. Technical Concept

- **Frontend:** mobile-first web app; rapid build via Lovable (prototype), then
  maintainable framework (Next.js/React) — responsive, works on low-end phones.
- **Backend / Database:** Supabase (Postgres + Auth + Storage + Realtime).
- **Maps:** Mapbox or Google Maps.
- **Risk engine:** deterministic, explainable scoring in SQL/edge functions
  (report volume, cluster density, verification confidence, signal
  combinations, historical baseline).
- **Authentication:** optional email/phone; anonymous reporting supported.
- **Deployment:** Vercel + Supabase.

The exact stack can change according to team implementation capacity. Locked
choices for this project: `context/architecture.md`, `specs/tech-selection.md`.

---

# 32. High-Level Architecture

```
                    RESIDENT
                       |
                       v
                CITIZEN APP  (web/mobile)
                       |
           +-----------+-----------+
           |                       |
           v                       v
        REPORT FORM             MAP + ALERTS
           |                       |
           +-----------+-----------+
                       |
                       v
                 SUPABASE BACKEND
        (reports · verifications · risk engine · alerts)
                       |
           +-----------+-----------+
           |                       |
           v                       v
     RISK SCORE ENGINE        GEO / BASELINE DATA
     (cluster + trend +      (areas · flooding · history)
      verification)
                       |
                       v
         ORGANIZATION DASHBOARD
         (hotspots · trends · prioritization)
```

---

# 33. Example Risk Calculation (illustrative)

Score components for an area (0–100):

- **Report volume vs baseline** (e.g. 3× normal within 7 days → large increase)
- **Cluster density** (reports concentrated within 1 km)
- **Verification confidence** (independent confirmations)
- **Signal mix** (water + sanitation + flooding + illness together weigh more)
- **Recency** (recent reports weigh more than old ones)

The system explains each component — e.g. "23 water reports · 8 sewage
incidents · recent flooding → HIGH (82/100)".

---

# 34. Design System

**Brand:** WaterWatch 💧. Communicate: community, early warning, local, clarity,
action, safety, trust.

**Design metaphor:** neighborhood maps, water droplets, signal/alert language,
community markers. Avoid a clinical, hospital-like aesthetic.

---

# 35. UI Style

Clear, calm, accessible, mobile-first, trustworthy, optimistic. Should feel like
a neighborhood watch for water — friendly and actionable, not alarming. Avoid:
fear-mongering, data-heavy corporate dashboards on the citizen side, dense
clinical UI.

---

# 36. Theme

Support light mode (primary for citizens outdoors) and dark mode (dashboards).
Thematic colors: **water blues** for the brand, **amber** for moderate risk,
**red** for high risk, **green** for low risk.

---

# 37. Landing Page Copy

- **Hero:** *See the risk. Share the signal. Protect the community.*
- **Subhead:** *WaterWatch turns local observations about water and sanitation
  into early warnings for your neighborhood.*
- **Primary CTA:** Report a Problem
- **Secondary CTA:** View Local Risk Map
- **Supporting message:** "Water problems often appear in your neighborhood long
  before they appear in the news. WaterWatch lets residents report what they
  see, verify each other's observations, and gives everyone a clearer picture of
  local WASH risk."

---

# 38. Brand Language

Preferred concepts: your neighborhood, your local area, early warning, signal,
report, verify, alert, risk level, hotspot, community, water safety, safe-water
sources.

Example: *"Someone near you reported brown water. Can you verify?"*

---

# 39. Pitch Structure

1. **Problem** — unsafe water, sanitation, flooding, and waterborne-disease risk
   in Myanmar; problems emerge at neighborhood level before official statistics
   see them.
2. **The gap** — people observe problems; organizations need information; no
   efficient bridge between them.
3. **Target users** — citizens (local alerts) and organizations (where to
   investigate first).
4. **Solution** — community-powered WASH early-warning platform producing
   neighborhood-level risk scores.
5. **How it works** — Observe → Report → Verify → Analyze → Alert → Prioritize.
6. **Why citizens participate** — information reciprocity, not volunteering for
   the greater good.
7. **Evidence** — WHO Yangon AWD outbreak; UNICEF WASH assessment; WHO early
   detection framework; mWater precedent.
8. **Product** — citizen app (Home / Report / Map / Alerts) + organization
   dashboard.
9. **Business model** — free citizen platform + paid WASH intelligence +
   sponsored WASH monitoring as a service.
10. **Viability** — useful information drives usage; intelligence drives
    payment; replication across cities; network effects.
11. **The ask** — US$10,000 pilot to answer three questions.
12. **Go-to-market** — pilot townships → data network → sell intelligence →
    expand.
13. **Team** — Team Compass.
14. **References** — WHO, UNICEF, mWater.

---

# 40. Core Product Loop

```
OBSERVE → REPORT → VERIFY → ANALYZE → ALERT → PRIORITIZE
```

An ongoing neighborhood early-warning system, not a one-time survey.

---

# 41. Long-Term Vision

From a Yangon pilot into a nationwide community WASH intelligence layer:

```
WATERWATCH → COMMUNITIES · ORGANIZATIONS → LOCAL RISK INTELLIGENCE →
EARLIER DETECTION · BETTER PRIORITIZATION → HEALTHIER COMMUNITIES
```

Ultimate vision: *Help every community see water and sanitation risks earlier —
and help responders act where it matters most.*

---

# 42. Project Scope Summary

**In scope:** community reporting, anonymous reporting, map visualization,
verification, risk scoring, citizen alerts, organization dashboard, hotspots,
trends, township-level aggregation.

**Future:** sponsored monitoring programs, multi-city expansion, sensor/rainfall
integration, partner rewards, export/API tiers, automated intelligence reports,
multi-language.

**Out of scope for MVP:** medical diagnosis, formal epidemiology, emergency
dispatch, citizen-government hotline integration, social network.

---

# 43. Core MVP Statement

> If residents provide observations about local water and sanitation, WaterWatch
> can combine, verify, and geographically analyze those observations to show
> communities where risk may be rising and organizations where to investigate
> first.

---

# 44. One-Sentence Description

> WaterWatch is a community-powered WASH early-warning platform that turns
> citizen observations about water and sanitation into location-based risk
> intelligence for waterborne-disease prevention.

---

# 45. Short Description

> WaterWatch lets residents report local water and sanitation problems, verify
> each other's observations, and receive localized alerts — while giving
> organizations a dashboard of where to prioritize investigation and response.

---

# 46. Tagline Options

- **Primary:** See the risk. Share the signal. Protect the community.
- **Short:** Your neighborhood's WASH early-warning system.
- **Action:** Report what you see. Warn your neighbors.
- **Bridge:** People who observe. Organizations that act. WaterWatch connects
  them.
- **Prevention:** From reactive outbreak response to proactive community-level
  prevention.

---

# 47. Project Keywords

WaterWatch · WASH · Water Safety · Sanitation · Early Warning System · Community
Reporting · Crowdsourced Risk Intelligence · Waterborne Disease · Cholera · AWD ·
Yangon · Myanmar · Civic Tech · Public Health · Flood Risk · Water Quality ·
Neighborhood Alerts · Risk Scoring · Community Engagement · Verification

---

# 48. Important Project Principle

WaterWatch does **not** tell users: *"Your area has a disease outbreak."*

Instead it says: *"Multiple residents have reported water problems near you.
This may be a sign that water quality is at risk. Consider precautions until the
situation is clarified."*

**The platform signals risk; communities and organizations make decisions.**

---

# 49. Final Product Vision

**WaterWatch 💧** — a trusted community early-warning layer that helps
residents: observe problems, share signals, verify what's real, understand local
risk, and act early — while helping organizations prioritize limited resources
where they matter most.

The goal is not to wait for an outbreak to become visible. The goal is to help
communities see the warning signs earlier.

---

# 50. Master Flow

```
OBSERVE → REPORT → VERIFY → ANALYZE → ALERT → PRIORITIZE
WATERWATCH 💧 → COMMUNITY SIGNALS → NEIGHBORHOOD RISK → LOCALIZED WARNINGS →
ORGANIZED RESPONSE → PREVENTION
```

**WaterWatch is therefore not simply a reporting app. It is a community WASH
intelligence layer that turns scattered observations into early warnings.**