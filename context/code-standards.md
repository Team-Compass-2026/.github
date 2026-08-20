# Code Standards — WaterWatch

**Team Compass🧭 · Active development (main app: Next.js + Neon; Lovable path: Supabase)**

## TypeScript
- `strict: true`; avoid `any`; prefer `unknown` + narrow
- Shared types from Zod (`z.infer`); `server-only` where needed
- ESM; match Next.js conventions

## Naming
- Components: `PascalCase.tsx` · hooks: `useCamelCase.ts`
- Server dirs: `kebab-case` / domain (`risk/`, `reports/`, `alerts/`)
- DB columns: `snake_case` (Prisma maps to Neon; Supabase tables `snake_case`)

## API & Zod
- Validate all inputs with Zod before logic (Hono `zValidator`)
- Consistent `{ data }` / `{ error: { code, message } }`
- Main app: session via Better Auth (`getCurrentUser`); write endpoints reject
  unauthenticated/rate-limited requests. Lovable path: Supabase RLS before writes
- Rate-limit report + verification submissions per user

## Database (main app: Prisma 7 + Neon)
- Migrations in `prisma/migrations/` via `bunx prisma migrate dev`; **always
  re-run `bunx prisma generate` after schema changes**
- Seed baseline areas + historical report rates in `prisma/seed.ts`
- Indexes on frequently filtered columns (`(areaId, createdAt)`, `(type, createdAt)`)

## Supabase / Postgres / PostGIS (Lovable path only)
- Migrations in `supabase/migrations/`; RLS policies required on every table
- Geospatial columns use PostGIS; indexes on `(township, created_at)` and
  geometry (GIST)
- Seed baseline areas + historical report rates in `supabase/seed.sql`

## Auth & Privacy
- Main app: **Better Auth** email/password (cookie session). Lovable path:
  Supabase Auth. **Anonymous reporting** supported everywhere
- PII minimal; identity/contact never exposed to organizations
- Reports are **signals, not diagnoses** — no medical fields

## Risk Engine / Structured Data
- Deterministic, explainable scoring (volume, cluster, verification, signal mix,
  recency) in `lib/risk.ts` (main app) / SQL views + edge functions (Lovable)
- Every score exposes a per-component breakdown ("why did this change?")
- LLM (if used later) explains signals only; the engine owns the math

## Testing (MVP)
- Unit: risk-score pure functions (volume/baseline, cluster, verification)
- Integration: report → verify → score flow; anonymous report path
- Security: unauthenticated write rejected; orgs can't read identity fields
- Manual: demo path (report → map → verify → alert → dashboard)

## Git / secrets
- `feat|fix|docs|chore|refactor|test(scope): why`
- Never commit `.env` / tokens / secrets (`.env` gitignored; `.env.example` documents vars)

## Lint / format
- ESLint (flat config, `bun run lint`) + `bunx tsc --noEmit`; CI: lint + typecheck + build

## Definition of Done
Spec met · types clean · access control enforced · signals-not-diagnoses copy ·
risk scores explainable · tests for touched logic · no secrets · progress-tracker
updated · demo path (report→verify→score→views) unbroken