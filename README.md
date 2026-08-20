# WaterWatch💧 — DEEP Hackathon 2026

**Team:** Team Compass 🧭 · **Project:** WaterWatch

## Overview

WaterWatch is a **community-powered WASH early-warning platform** for
waterborne-disease risk. Citizens report local water and sanitation problems
(dirty water, sewage overflow, flooding, broken infrastructure, unsafe
sanitation, unusual illness in the community), and WaterWatch turns those
observations into **neighborhood-level risk intelligence** that communities and
organizations can act on.

Journey: **Observe → Report → Verify → Analyze → Alert → Prioritize**

One-line pitch: *Turning community observations into early warnings for
waterborne-disease risk.*

Tagline: **See the risk. Share the signal. Protect the community.** · *Myanmar's
community WASH intelligence layer.*

## Repositories

- **[waterwatch](https://github.com/Team-Compass-2026/waterwatch)** — the product
  codebase (citizen app + organization dashboard; Next.js 16 + Neon Postgres +
  Better Auth + Hono + React Query, with a Lovable/Supabase prototype path).
  `README.md` there describes the product and app setup.
- **[.github](https://github.com/Team-Compass-2026/.github)** — this org repo:
  org profile, issue/PR templates, and shared project context.

## Context & Docs

The `context/` folder holds the canonical project documentation:

- `context/product-spec.md` — the full WaterWatch master specification (problem,
  gap, users, solution, six-step flow, incentive model, research, product,
  business model, pilot budget, go-to-market, pitch)
- `context/prototype-spec.md` — high-fidelity clickable prototype brief (citizen
  app: Home → Report → Map → Alerts; + organization dashboard)
- `context/project-setup.md` — onboarding guide, version/lifecycle management,
  daily workflow
- `context/project-overview.md` — product definition, goals, features, scope
- `context/architecture.md` — system structure, storage model, risk engine,
  invariants
- `context/ui-context.md` — theme, colors, typography, component conventions
- `context/code-standards.md` — implementation rules and conventions
- `context/ai-workflow-rules.md` — development workflow, scoping, delivery
  approach
- `context/progress-tracker.md` — current phase, completed work, next steps
- `context/specs/` — optional unit specs (one file per feature)

## Repository Structure (this repo)

- `context/` — shared project context and specs
- `workflows/` — CI/CD and automation workflows
- `ISSUE_TEMPLATE/` — issue reporting templates
- `pull_request_template/` — PR guidance

## Quick Setup

```bash
# Clone the org repo
git clone https://github.com/Team-Compass-2026/.github.git

# Clone the product repo
git clone https://github.com/Team-Compass-2026/waterwatch.git
cd waterwatch
bun install
bun run dev
```