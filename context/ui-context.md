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
- Brand descriptor: *Turning community observations into early warnings for waterborne-disease risk*
- Brand mark: **WATERWATCH** (stylized/hero)

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

**Navy-dominant. Blue leads. Red only for risk/alerts — never a major brand color.**
Fonts: Space Grotesk (headings) / DM Sans (body) / Geist Mono (data only).
Visual style: Google Maps × WHO dashboard × modern startup — rounded cards, thin borders, whitespace, simple line icons, map visuals, small data-viz, minimal gradients.
Avoid: illustrations, cartoonish graphics, too many colors, dense paragraphs, stock photos.

Light theme:
```
background: '#F7F9FA'              /* Off-white */
surface: '#FFFFFF'
surface-muted: '#EEF2F5'
surface-subtle: '#F7F9FA'
surface-hover: '#EEF2F5'

text-primary: '#1F2933'            /* Dark Charcoal */
text-secondary: '#475569'
text-muted: '#64748B'
text-disabled: '#94A3B8'

border: '#E3E8EE'
border-strong: '#CBD5E1'

primary: '#123B5D'                 /* Deep Navy — brand lead */
primary-hover: '#0F3150'
primary-active: '#0B2741'
primary-soft: '#E3EBF3'
on-primary: '#FFFFFF'

secondary: '#2F80ED'               /* Water Blue — links, map pins */
secondary-hover: '#2B74D6'
secondary-active: '#2565BA'
secondary-soft: '#EAF2FE'
secondary-container: '#D6E6FB'
on-secondary: '#FFFFFF'

destructive: '#EB5757'             /* Coral Red — risk/alerts ONLY */
destructive-soft: '#FDEBEB'

success: '#27AE60'
success-soft: '#E6F7EE'

warning / moderate-risk: '#D97706'
warning-soft: '#FEF3C7'

danger / high-risk: '#DC2626'
danger-soft: '#FEE2E2'

critical: '#B91C1C'
critical-soft: '#FECACA'

ring: '#2F80ED'
input: '#CBD5E1'

inverse-surface: '#1F2933'
inverse-text: '#F7F9FA'
```

DARK THEME:
```
background: '#0F1B26'
surface: '#152230'
surface-muted: '#1B2A3A'
surface-subtle: '#0F1B26'
surface-hover: '#233445'

text-primary: '#E8EFF5'
text-secondary: '#CBD5E1'
text-muted: '#8FA0B0'
text-disabled: '#64748B'

border: '#233445'
border-strong: '#334155'

primary: '#2F80ED'                 /* Water Blue — dark mode */
primary-hover: '#2B74D6'
primary-active: '#2565BA'
primary-soft: '#1B2A3A'
on-primary: '#FFFFFF'

secondary: '#123B5D'               /* Navy — dark mode secondary */
secondary-hover: '#0F3150'
on-secondary: '#FFFFFF'

destructive: '#EB5757'
destructive-soft: '#3D1515'

success: '#4ADE80'
success-soft: '#14532D'

warning / moderate-risk: '#FBBF24'
warning-soft: '#451A03'

danger / high-risk: '#F87171'
danger-soft: '#450A0A'

critical: '#EF4444'
critical-soft: '#7F1D1D'

ring: '#2F80ED'
input: '#233445'

inverse-surface: '#E8EFF5'
inverse-text: '#0F1B26'
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