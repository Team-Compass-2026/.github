# Team Compass🧭 — DEEP Hackathon 2026

**Track:** T2 — Education Equity

**Project:** Career GPS — Career navigation for young people.

## Overview

Career GPS turns scattered career information into a clear, personalized, actionable roadmap. It combines a structured career→skills→resources dataset, user profiles, and skill-gap analysis.

Journey: **Confusion → Understanding → Planning → Learning → Action → Career Readiness**

One-line pitch: *Helps young people turn overwhelming career information into a personalized, evidence-based roadmap for what to learn and do next.*

## Repositories

- **[career-gps](https://github.com/Team-Compass-2026/career-gps)** — the product codebase (Next.js + Prisma + Hono, Better Auth). `README.md` there describes the product and app setup.
- **[.github](https://github.com/Team-Compass-2026/.github)** — this org repo: org profile, issue/PR templates, and shared project context.

## Context & Docs

The `context/` folder holds the canonical project documentation:

- `context/project-setup.md` — onboarding guide, version/lifecycle management, daily workflow
- `context/project-overview.md` — product definition, goals, features, scope
- `context/architecture.md` — system structure, storage model, invariants
- `context/ui-context.md` — theme, colors, typography, component conventions
- `context/code-standards.md` — implementation rules and conventions
- `context/ai-workflow-rules.md` — development workflow, scoping, delivery approach
- `context/progress-tracker.md` — current phase, completed work, next steps
- `context/specs/` — optional unit specs (one file per feature)

See also `docs/architecture/` and `docs/product/DEEP-hackathon-overview.md` in the `career-gps` repo.

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
git clone https://github.com/Team-Compass-2026/career-gps.git
cd career-gps
bun install
bun run dev
```