# Prototype Development Spec — WaterWatch

**Brand:** WaterWatch · **Team:** Team Compass 🧭 · **Hackathon:** DEEP 2026

Goal: build a high-fidelity **clickable web/mobile prototype** of the WaterWatch
community WASH early-warning platform for the hackathon demo. The product is a
community-powered early-warning platform: citizens report local water and
sanitation problems; organizations receive location-based risk intelligence.

> Brand = **WaterWatch**. Canonical design tokens implemented in the app live in
> `context/ui-context.md` and `app/globals.css`. This file is the prototype
> development brief (page-by-page).

---

## Product Concept

The platform bridges residents who observe problems with organizations that need
information. Instead of simply collecting complaints, the platform:

1. Lets residents report a WASH problem (what / where / when / photo).
2. Shows reports on a neighborhood map.
3. Lets nearby users verify or dispute reports.
4. Computes a neighborhood-level WASH Risk Score.
5. Sends localized alerts to citizens.
6. Gives organizations a prioritization dashboard (hotspots + trends).

The product should NOT feel like:
- A clinical hospital system
- A government hotline form
- A generic survey tool
- A fear-mongering outbreak tracker
- A dense data-heavy corporate dashboard (on the citizen side)

## Target Users

Primary users (citizen app):
- Yangon residents
- Families in flood/sanitation-vulnerable areas
- Students and young adults
- Community volunteers
- Residents dependent on local water sources or vendors

Secondary users (organization dashboard):
- NGOs, humanitarian and WASH organizations
- Clinics and health facilities
- Researchers
- Water-service providers
- Local authorities

## User Experience

The experience should feel: **Simple · Local · Calm · Trustworthy · Actionable ·
Empowering · Optimistic**

On the citizen side, low friction and mobile-first. On the organization side,
clear prioritization over raw data.

## Visual Style

Create a polished contemporary digital product with a community-friendly
aesthetic. Use:
- Clean modern typography
- Strong visual hierarchy
- Rounded cards with restrained corner radius
- Subtle borders and light shadows
- Clear primary and secondary buttons
- High-quality icons (report types, map markers, alerts)
- Consistent spacing and alignment

## Color System

Use a palette that communicates water safety and risk levels.
- **Water blues** — brand (trust, water)
- **Green** — low risk / safe water
- **Amber** — moderate risk
- **Red** — high risk
- **White / soft surfaces** — clean and tidy

Do not introduce arbitrary colors that conflict with the brand or the risk
semantics. Risk color (green / amber / red) must never be used for anything
other than risk level so meaning stays unambiguous.

## Typography

Use a modern, highly legible sans-serif typeface with a clear hierarchy:

- **H1** — Large, confident, highly readable.
- **H2** — Strong section heading.
- **H3** — Card or subsection heading.
- **Body** — Highly readable with comfortable line height.
- **Caption** — Smaller muted text.

## Layout

Mobile-first responsive layout for the citizen app (primary demo device: phone
viewport), desktop layout for the organization dashboard.

Citizen app primary navigation (bottom tabs on mobile):
- Home (Your area)
- Map
- Report
- Alerts
- Profile

## Component Consistency

Create reusable components for: report-type chips, risk-level badges, map
markers, alert cards, report cards, verification buttons (confirm/dispute),
location pickers, photo upload, township/area cards, trend indicators, hotspot
rows, data-table rows.

The same component must look identical across all pages.

## Important Prototype Rule

Do not invent major product features that are not specified.

Do not add: medical diagnoses, disease outbreak claims, emergency dispatch,
chat/social feeds, cryptocurrency, e-commerce, complex admin panels on the
citizen side.

The prototype should focus on the core Observe → Report → Verify → Alert →
Prioritize experience.

## Content Rule

Use realistic prototype data (e.g. a Hlaing Tharyar neighborhood example).

Where content is intentionally unspecified, use clearly marked placeholders such
as: `[TOWNSHIP]`, `[AREA]`, `[REPORT TYPE]`, `[DISTANCE]`, `[PHOTO]`, `[RISK
SCORE]`, `[ORG NAME]`.

## Interaction Design

The prototype must be clickable. Important buttons should navigate to the
appropriate next screen. The primary user journey:

```
LANDING → HOME (Your area) → REPORT → SUBMIT → MAP → VERIFY (nearby) → ALERTS
```

And the organization journey:

```
ORG LOGIN → DASHBOARD (overall risk) → HOTSPOT LIST → HOTSPOT DETAIL (reports)
```

Interactions should feel intentional rather than decorative.

## Accessibility

Maintain: strong text contrast, clear button labels, sufficient spacing,
readable font sizes, distinguishable states, logical keyboard-style navigation
hierarchy. Never communicate risk through color alone (always pair with a
label/badge text).

---

# Page Layouts

## 1. Landing Page

**Navigation:** How It Works · Map · For Organizations · **Button:** Report a
Problem

**Hero — Left**
- Headline: *See the risk. Share the signal. Protect the community.*
- Brand descriptor: *Turning community observations into early warnings for waterborne-disease risk*
- Subheadline: *WaterWatch turns local observations about water and sanitation
  into early warnings for your neighborhood.*
- Primary CTA: **Report a Problem**
- Secondary CTA: **View Local Risk Map**

**Hero — Right graphic:** WaterWatch neighborhood risk visualization:

```
YOUR AREA
Hlaing Tharyar
WASH Risk: 🟠 MODERATE (54/100)
Reports this week: 8
↓
Map with colored area overlays
(🔴 high · 🟠 moderate · 🟢 low)
```

**Below hero — How it works**
- 01 — **Observe**: Notice dirty water, sewage, flooding, or broken
  infrastructure.
- 02 — **Report**: Tell us what, where, and when. Add a photo.
- 03 — **Verify**: Nearby residents confirm or dispute reports.
- 04 — **Alert**: Get localized warnings and see neighborhood risk.

**Below that — Three benefits**
- **Know Your Neighborhood** — See the current WASH risk around you.
- **Warn Your Neighbors** — Your report helps people nearby stay safe.
- **Guide the Response** — Organizations use the signals to prioritize where to
  investigate.

**Final CTA:** Ready to see what's happening near you? **View Local Risk Map →**

## 2. Home — Your Area

**Header:** [YOUR AREA] · location + current risk badge

- **Top card — Your Area**
  - WASH Risk: 🟠 MODERATE
  - Risk score: 54/100
  - Recent reports: 8 (this week)
  - Trend: ↑ 12% vs last week
- **Why this score?** (expandable)
  - 5 water-quality reports
  - 2 sewage incidents
  - 1 recent flooding report
- **Local recommendations card**
  - *"Multiple water-quality concerns reported near you. Consider using
    treated/boiled drinking water until the situation is clarified."*
- **Nearby hotspots list:** [AREA] — 🟠 54/100 · [AREA] — 🔴 82/100 · [AREA] —
  🟢 22/100
- **Bottom actions:** [Report a Problem] · [View Map]

## 3. Report a Problem

**Header:** Report a Problem
**Subtext:** What did you observe?

**Step 1 — Type**
○ Unsafe water
○ Sewage
○ Flooding
○ Broken infrastructure
○ Sanitation problem
○ Illness cluster
○ Other

**Step 2 — Location**
📍 Map pin / use my location · [TOWNSHIP / AREA auto-detected]

**Step 3 — Details**
- When did this happen? (Today / This week / Other)
- Optional note: [TEXT]
- 📷 Add photo (optional)

**Step 4 — Privacy**
- ☐ Report anonymously
- ☐ I am a WaterWatch Guardian (optional)

**Bottom:** [SUBMIT]

**After submit:** confirmation card + "Help verify nearby reports" prompt →
`Map` screen.

## 4. Map

A live neighborhood map showing:
- 🔴 High-risk areas
- 🟠 Moderate-risk areas
- 🟢 Low-risk areas

**Report markers** (latest N reports with type icons):
- 💧 Unsafe water · 🧯 Sewage · 🌊 Flooding · 🔧 Broken infrastructure ·
  🚻 Sanitation · 🤒 Illness cluster · ·  Other

**Interaction:** tap an area → bottom sheet with:
- Area name + risk score + trend
- Why the score changed (report mix)
- Recent report list (type, time, verification count)
- [Verify nearby reports] button

**Bottom floating button:** [Report a Problem]

## 5. Alerts

**Header:** Alerts

**Alert card — Elevated risk detected near you**
> Multiple residents have reported water-quality problems in your area.
> Consider using treated/boiled drinking water until the situation is clarified.

- Severity badge: 🟠 MODERATE / 🔴 HIGH
- Area: [TOWNSHIP]
- Time: [RELATIVE]
- [View map] · [Verify reports]

**Alert card — Verification request**
> "Brown water reported at this location." — [DISTANCE] from you
> [CONFIRM] [DISPUTE] [NOT SURE]

**Alert card — Neighborhood update**
> Reported sewage overflow has been confirmed by 3 neighbors.

## 6. Profile / Contribution

**Header:** Profile

- **Reputation:** Community Badges (e.g. WaterWatch Guardian, Verified Reporter)
- **My reports:** list with status (open / verified / resolved)
- **My verifications:** count
- **Settings:** location, alert preferences, language, anonymous default
- **Partner rewards (future, disabled):** "Coming soon — earn points for verified
  contributions."

## 7. Organization Dashboard (desktop)

**Header:** Yangon WASH Intelligence Dashboard
**Org:** [ORG NAME] · Region: Yangon

**Top — Overall risk:** 71/100 · 🟠 HIGH

| **Indicator**         | **Current** | **Trend** |
| --------------------- | ----------- | --------- |
| Water reports         | 247         | ↑ 38%     |
| Sanitation reports    | 84          | ↑ 61%     |
| Illness signals       | 129         | ↑ 72%     |
| Flood-related reports | 31          | ↑ 24%     |

**AI-generated priority areas**
1. **Township A — HIGH (87/100)** — click → hotspot detail
2. **Township B — HIGH (79/100)**
3. **Township C — MODERATE (73/100)**

**Hotspot detail (drill-down):**
- Risk score + trend (↑ 41%)
- Signal breakdown: water 37 · sanitation 12 · illness ↑ · flooding yes
- Recent reports table (type, time, verification, township)
- Filters: date range · report type · township · verification status
- [Export] · [Subscribe to alerts]

**Navigation:** Overview · Hotspots · Reports · Trends · Settings