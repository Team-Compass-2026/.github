# Landing Page Plan — WaterWatch

**Product:** WaterWatch · **Team:** Team Compass🧭 · **Hackathon:** DEEP 2026

## Brand Integration

- **Product name:** WaterWatch (hero-level on marketing)
- **Tagline:** See the risk. Share the signal. Protect the community.
- **Brand descriptor:** Turning community observations into early warnings for waterborne-disease risk
- **Brand mark:** WATERWATCH (hero/logo contexts)
- **Short tagline:** Myanmar's community WASH intelligence layer.
- **Theme:** Community Early Warning · Neighborhood watch for water
- **Visual language:** Community → Signal → Clarity → Early Warning → Safety → Trust

## Color System — WaterWatch Palette

Brand colors per design system (`context/ui-context.md`):
- **Water Blue** — brand/trust (primary CTA, active states)
- **Green** — low risk / safe water
- **Amber** — moderate risk
- **Red** — high risk
- **White / soft surfaces** — clean and tidy (backgrounds, cards)

Risk colors are used **only** for risk levels and always paired with a label +
score (never color alone).

```
LIGHT THEME:
background: '#F8FAFC'
surface: '#FFFFFF'
surface-muted: '#F1F5F9'
surface-subtle: '#F8FAFC'
surface-hover: '#F1F5F9'

text-primary: '#0F172A'
text-secondary: '#475569'
text-muted: '#64748B'

primary: '#0284C7'          /* Water Blue */
primary-hover: '#0369A1'
primary-active: '#075985'
primary-soft: '#E0F2FE'
primary-container: '#BAE6FD'
on-primary: '#FFFFFF'

secondary: '#0F172A'
on-secondary: '#FFFFFF'

success/low-risk: '#16A34A'
warning/moderate-risk: '#F59E0B'
danger/high-risk: '#DC2626'

water: '#0EA5E9'
water-soft: '#E0F2FE'

inverse-surface: '#0F172A'
inverse-text: '#F8FAFC'

DARK THEME:
background: '#0B1120'
surface: '#111827'
surface-muted: '#172033'
surface-subtle: '#0F172A'
surface-hover: '#1E293B'

text-primary: '#F8FAFC'
text-secondary: '#CBD5E1'
text-muted: '#94A3B8'

primary: '#38BDF8'          /* Water Blue - dark */
primary-hover: '#7DD3FC'
primary-active: '#0EA5E9'
primary-soft: '#0C4A6E'
primary-container: '#075985'
on-primary: '#082F49'

secondary: '#F8FAFC'
on-secondary: '#0F172A'

success/low-risk: '#4ADE80'
warning/moderate-risk: '#FBBF24'
danger/high-risk: '#F87171'

water: '#38BDF8'
water-soft: '#0C4A6E'

inverse-surface: '#F8FAFC'
inverse-text: '#0F172A'
```

## Typography — WaterWatch

Font family: **Plus Jakarta Sans** (or equivalent modern legible sans)

```
hero-display:     56px  800  '64px'  '-0.02em'
hero-display-mobile: 34px  800  '42px'  '-0.02em'

headline-xl: 40px  800  '48px'  '-0.02em'
headline-lg:  30px  700  '38px'
headline-md:  22px  700  '30px'
title-lg:     18px  700  '26px'

body-lg:  17px  400  '27px'
body-md:  15px  400  '23px'
body-sm:  13px  400  '19px'

label:    14px  600  '20px'
label-caps: 12px  600  '16px'  '0.05em'
```

## Layout System

- **Mobile-first** (citizen app primary)
- **12-column desktop grid** for org dashboard
- **Max content width:** 1280px (dashboard) / 480px (mobile)
- **8px spacing system** — all major spacing multiples of 8

**Section rhythm (Landing page):**
- Desktop: 96–112px vertical spacing
- Tablet: 80px
- Mobile: 56px

## Hero Section — WaterWatch

### Left Side

**Headline:**
See the risk. Share the signal. Protect the community.

**Subheadline:**
WaterWatch turns local observations about water and sanitation into early
warnings for your neighborhood.

**Primary CTA:** Report a Problem
**Secondary CTA:** View Local Risk Map

### Right Side — Neighborhood Risk Visualization

```
YOUR AREA
Hlaing Tharyar
WASH Risk: 🟠 MODERATE (54/100)
Reports this week: 8
↓
Map with colored area overlays
🔴 HIGH · 🟠 MODERATE · 🟢 LOW
```

## How It Works

01 — **Observe**: Notice dirty water, sewage, flooding, or broken
infrastructure.
02 — **Report**: Tell us what, where, and when. Add a photo.
03 — **Verify**: Nearby residents confirm or dispute reports.
04 — **Alert**: Get localized warnings and see neighborhood risk.

## Three Benefits Section

**Know Your Neighborhood**
See the current WASH risk around you — and why it changed.

**Warn Your Neighbors**
Your report helps people nearby stay safe, verified by the community.

**Guide the Response**
Organizations use the signals to prioritize where to investigate first.

**Final CTA:** Ready to see what's happening near you? **View Local Risk Map →**

## Navigation

**Primary navigation (landing):**
- Logo (WaterWatch)
- How It Works
- Map
- For Organizations
- **Report a Problem** (button)

**Citizen app tabs (in-app):** Home · Map · Report · Alerts · Profile

**Light mode nav:** `rgba(255,255,255,0.82)` with `backdrop-filter: blur(12px)`
**Dark mode nav:** `rgba(11,17,32,0.82)` with `backdrop-filter: blur(12px)`

## Content & Placeholders

Where content is intentionally unspecified, use clearly marked placeholders:

[TOWNSHIP] [AREA] [REPORT TYPE] [DISTANCE] [PHOTO] [RISK SCORE] [ORG NAME]

## Interactions

- Primary buttons: Water Blue background, white text, 16px radius
- Hover: slight upward movement, slightly darker blue, soft shadow
- Cards: 16–20px radius, subtle shadow, lift on hover (`translateY(-4px)`)
- Map areas: colored overlays; tapping opens the area detail sheet
- Report submit: success confirmation → prompt to verify nearby reports

## Accessibility

- WCAG-friendly contrast
- Visible focus states
- Keyboard navigation
- Minimum 44px touch targets
- Semantic headings
- Alt text
- Reduced-motion support
- Risk levels never communicated by color alone (badge + score always)

## Primary User Journey

LANDING → HOME (Your area) → REPORT → SUBMIT → MAP → VERIFY → ALERTS

Organization journey: ORG LOGIN → DASHBOARD → HOTSPOTS → HOTSPOT DETAIL

> Full page-by-page prototype brief: `context/prototype-spec.md`. The MVP core
> (see `context/product-spec.md`) is the five things only: report, map, verify,
> basic risk score, two views.

## Dark Mode Support

Full dark mode support per design system:
- Suitable for organization dashboard, hotspot drill-downs, trends
- Background: `#0B1120`
- Cards: `#111827`
- Primary text: `#F8FAFC`
- Accent: `#38BDF8`

## Signature Interaction — Area Risk Pulse

When users open the map or a risk card, the target area overlay pulses from its
current risk color, and the score card expands into its component breakdown
(volume · cluster · verification · signal mix · recency). This becomes
WaterWatch's recognizable interaction pattern — *always explainable*.

## Brand Voice in UI

Use language that is:
- Clear
- Local
- Encouraging
- Practical
- Calm (informative, not alarming)

Preferred (early-warning language):
- **Report a Problem** instead of Submit a Complaint
- **Confirm / Dispute** instead of Validate / Reject
- **See Why** (risk explanation) instead of View Analytics
- **Get a Local Alert** instead of Enable Notifications
- **Safe-water advice** instead of Medical Guidance

## Final Brand Feeling

When someone visits WaterWatch, they should feel:
1. "I understand what's happening near me."
2. "I can do something about it easily."
3. "Neighbors are watching out for each other."
4. "Responders know where to focus."

**Team Compass 🧭 — See the risk. Share the signal. Protect the community.**