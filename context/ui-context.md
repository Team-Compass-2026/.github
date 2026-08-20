# UI Context — WaterWatch

## Product feel

Calm, clear, local, community-driven. Emphasize **neighborhood awareness and
next actions**. Avoid fear-mongering, clinical/hospital aesthetics, and dense
data-heavy dashboards on the citizen side. Risk states are informative, not
alarming.

## Brand

- Product name **WaterWatch** is hero-level on marketing
- Team Compass🧭 secondary (about / footer)
- Primary tagline: **See the risk. Share the signal. Protect the community.**
- Short tagline: **Myanmar's community WASH intelligence layer.**

## Theme — Community Early Warning

Product should feel like: **a neighborhood watch for water** — mobile-first,
friendly, actionable — not a hospital system or a government portal.

Visual language communicates: **Community → Signal → Clarity → Early Warning →
Safety → Trust**

Emotional journey:
- "I noticed something wrong with the water." → "I can report it easily." →
  "I can see what's happening near me." → "I know what to do."

## Report-Type Icons

Always pair an icon with a label:

- 💧 Unsafe water
- 🧯 Sewage
- 🌊 Flooding
- 🔧 Broken infrastructure
- 🚻 Sanitation problem
- 🤒 Illness cluster
- ⚪ Other

## Risk Semantics (must be consistent)

Risk level is always a **color + badge label + score** — never color alone.

- 🟢 **LOW** (0–33) — green
- 🟠 **MODERATE** (34–66) — amber
- 🔴 **HIGH** (67–100) — red

Use these risk colors only for risk levels, so meaning stays unambiguous.

## Theme Strategy

### Light Mode — Primary Experience

Default for: Citizen app (used outdoors), Landing, Map, Home, Report, Alerts
Overall experience: bright, optimistic, welcoming

**White + soft blue-gray + water blue + green/amber/red risk accents.**
Do not use pure black backgrounds.

### Dark Mode — Product / Focus Experience

Supported. Feel: **Professional + Focused**. Dark navy surfaces instead of pure
black. Suitable for: Organization dashboard, hotspot drill-downs, trends.

## Color System — WaterWatch Palette

Light theme:
```
background: '#F8FAFC'
surface: '#FFFFFF'
surface-muted: '#F1F5F9'
surface-subtle: '#F8FAFC'
surface-hover: '#F1F5F9'

text-primary: '#0F172A'
text-secondary: '#475569'
text-muted: '#64748B'
text-disabled: '#94A3B8'

border: '#E2E8F0'
border-strong: '#CBD5E1'

primary: '#0284C7'          /* Water Blue */
primary-hover: '#0369A1'
primary-active: '#075985'
primary-soft: '#E0F2FE'
primary-container: '#BAE6FD'
on-primary: '#FFFFFF'

secondary: '#0F172A'
on-secondary: '#FFFFFF'

success / low-risk: '#16A34A'
success-soft: '#DCFCE7'
on-success: '#052E16'

warning / moderate-risk: '#F59E0B'
warning-soft: '#FEF3C7'
on-warning: '#451A03'

danger / high-risk: '#DC2626'
danger-soft: '#FEE2E2'
on-danger: '#450A0A'

water: '#0EA5E9'
water-soft: '#E0F2FE'

inverse-surface: '#0F172A'
inverse-text: '#F8FAFC'
```

DARK THEME:
```
background: '#0B1120'
surface: '#111827'
surface-muted: '#172033'
surface-subtle: '#0F172A'
surface-hover: '#1E293B'

text-primary: '#F8FAFC'
text-secondary: '#CBD5E1'
text-muted: '#94A3B8'
text-disabled: '#64748B'

border: '#263449'
border-strong: '#334155'

primary: '#38BDF8'          /* Water Blue - dark */
primary-hover: '#7DD3FC'
primary-active: '#0EA5E9'
primary-soft: '#0C4A6E'
primary-container: '#075985'
on-primary: '#082F49'

secondary: '#F8FAFC'
on-secondary: '#0F172A'

success / low-risk: '#4ADE80'
success-soft: '#14532D'
on-success: '#052E16'

warning / moderate-risk: '#FBBF24'
warning-soft: '#451A03'
on-warning: '#FFFBEB'

danger / high-risk: '#F87171'
danger-soft: '#450A0A'
on-danger: '#FFFBEB'

water: '#38BDF8'
water-soft: '#0C4A6E'

inverse-surface: '#F8FAFC'
inverse-text: '#0F172A'
```

## Typography

fontFamily: 'Plus Jakarta Sans' (or an equally legible modern sans-serif)

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

- **Mobile-first** — citizen app bottom-tab navigation (Home · Map · Report ·
  Alerts · Profile)
- **12-column desktop grid** for the organization dashboard
- **Max content width:** 1280px (dashboard) / 480px (mobile app)
- **8px spacing system** — all major spacing values multiples of 8

**Section rhythm (Landing page):**
- Desktop: 96–112px vertical spacing
- Tablet: 80px
- Mobile: 56px

## Key screens (MVP)

1. Landing — brand, one headline, one CTA, neighborhood risk visualization
2. Home (Your area) — risk score + why + recommendations
3. Report — type, location, details, photo, anonymous option
4. Map — area overlays + report markers + area detail sheet
5. Alerts — localized warnings + verification requests
6. Profile — reputation, my reports, settings
7. Organization dashboard — overall risk, indicators, hotspots, drill-down

## Responsive

- Mobile: citizen app full experience; report-first; map in sheet/tab
- Desktop: organization dashboard with side-by-side hotspot + report table