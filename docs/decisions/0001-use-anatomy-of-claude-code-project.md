# 0001: Adopt the Anatomy of a Claude Code Project structure

Date: 2026-05-07
Status: Accepted

## Context
This sandbox initially had a flat structure (CLAUDE.md, README.md, index.html, workflow file). As Salescake CRM and Power Upgrade Solar repos grow under the `salescakecrm` org, we need a consistent structure so Claude has reliable context everywhere it works.

## Decision
Adopt the "Anatomy of a Claude Code Project" pattern across all repos in `salescakecrm`:
- Structured `CLAUDE.md` with explicit Purpose / Repo Map / Rules / Workflows sections
- `.claude/skills/` for reusable expert workflows
- `.claude/hooks/` for deterministic guardrails
- `docs/` directory with `architecture.md`, `decisions/` (ADRs), `runbooks/`
- Module-local `CLAUDE.md` files inside risky modules (auth, billing, migrations)

## Consequences
- New repos created from `salescakecrm` follow this pattern from day one
- Existing sandbox repo restructured retroactively (this PR)
- Future ADRs are numbered 0002-, 0003-, ... in `docs/decisions/`
