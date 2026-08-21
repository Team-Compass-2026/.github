# AI Agent Notes — WaterWatch Org Repo

## Repositories

- **civic-alert-system/** — MAIN APP (TanStack Start + React 19 + Tailwind v4 +
  Supabase). This is the active delivery path; deployed at
  https://civic-alert-system-theta.vercel.app/
- **waterwatch-nextjs/** — ARCHIVED prototype (Next.js 16 + Neon Postgres +
  Prisma + Better Auth + Hono). Reference only — do not develop here.

## Context read order

1. `context/project-overview.md` — what the product is
2. `context/architecture.md` — system structure, data model
3. `context/code-standards.md` — conventions, gates
4. `context/ui-context.md` — tokens, palette, typography
5. `context/ai-workflow-rules.md` — how to scope and deliver
6. `context/progress-tracker.md` — current state, what's next

## Orchestra commands

- `/orchestra off` — disable auto-orchestra
- `/orchestra on` — enable auto-orchestra
- `/orchestra stop` — halt running orchestra loop

## Notes

- `context/product-spec.md` holds the master product specification
- Each nested repo has its own `context/` and `AGENTS.md` for local context
- `civic-alert-system/` = main app (TanStack Start + Supabase) — all feature work happens here
- `waterwatch-nextjs/` = archived Next.js prototype — kept for design/data-model reference only
