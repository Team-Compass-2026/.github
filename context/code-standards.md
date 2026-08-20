# Code Standards — WaterWatch

**Team Compass🧭 · Apply when build starts (no scaffold yet)**

## TypeScript
- `strict: true`; avoid `any`; prefer `unknown` + narrow
- Shared types from Zod (`z.infer`); `server-only` where needed
- ESM; match Next + Supabase conventions

## Naming
- Components: `PascalCase.tsx` · hooks: `useCamelCase.ts`
- Server dirs: `kebab-case` / domain (`risk/`, `reports/`, `alerts/`)
- Supabase tables: `snake_case` names, `snake_case` columns

## API & Zod
- Validate all inputs with Zod before logic
- Consistent `{ data }` / `{ error: { code, message } }`
- Supabase RLS before writes; `401`/`403` if unauthorized
- Rate-limit report + verification submissions per user

## Supabase / Postgres / PostGIS
- Migrations in `supabase/migrations/`; RLS policies required on every table
- Geospatial columns use PostGIS; indexes on `(township, created_at)` and
  geometry (GIST)
- Seed baseline areas + historical report rates in `supabase/seed.sql`

## Auth & Privacy
- Supabase Auth email/phone; **anonymous reporting** supported
- PII minimal; identity/contact never exposed to organizations (RLS)
- Reports are **signals, not diagnoses** — no medical fields

## Risk Engine / Structured Data
- Deterministic, explainable scoring (volume, cluster, verification, signal mix,
  recency) in SQL views / edge functions
- Every score exposes a per-component breakdown ("why did this change?")
- LLM (if used later) explains signals only; the engine owns the math

## Testing (MVP)
- Unit: risk-score pure functions (volume/baseline, cluster, verification)
- Integration: report → verify → score flow; anonymous report path
- Security: RLS policies — unauthenticated write rejected; orgs can't read
  identity fields
- Manual: demo path (report → map → verify → alert → dashboard)

## Git / secrets
- `feat|fix|docs|chore|refactor|test(scope): why`
- Never commit `.env` / tokens / Supabase service keys

## Lint / format
- ESLint + Prettier **or** Biome once scaffolded; CI: lint + typecheck

## Definition of Done
Spec met · types clean · RLS/tenancy · signals-not-diagnoses copy · risk scores
explainable · tests for touched logic · no secrets · progress-tracker updated ·
demo path (report→verify→score→views) unbroken