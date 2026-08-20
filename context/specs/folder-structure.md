# Folder Structure (full MVP proposal)

See also: `docs/architecture/folder-structure.md`

```text
waterwatch/
├── app/
│   ├── layout.tsx
│   ├── globals.css
│   ├── page.tsx              # Landing page (marketing)
│   ├── (citizen)/
│   │   ├── home/             # Your area — risk score + why
│   │   ├── report/           # Report a WASH problem
│   │   ├── map/              # Neighborhood map + area detail
│   │   ├── alerts/           # Localized alerts + verification
│   │   └── profile/          # Reputation, my reports, settings
│   └── (org)/
│       ├── dashboard/        # Overall risk + indicators
│       ├── hotspots/         # Priority areas list
│       ├── hotspots/[area]/  # Drill-down to reports
│       ├── trends/
│       └── settings/
├── components/
│   ├── ui/
│   ├── report-cards/
│   ├── risk-badges/
│   ├── map/
│   ├── alert-cards/
│   └── navigation/
├── lib/
│   ├── validations/          # Zod schemas
│   ├── risk/                 # risk-score pure functions
│   └── supabase/             # client/server + RPC helpers
├── supabase/
│   ├── migrations/
│   ├── seed.sql              # pilot townships + baselines
│   ├── functions/            # edge functions
│   └── storage/
├── public/                   # report photos bucket mirror config
├── context/ · docs/ · .cursor/skills/
├── next.config.js
├── tailwind.config.js
├── package.json
└── .env.example
```

**Scaffold only when product owner says build.**