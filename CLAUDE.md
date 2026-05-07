# claude-github-sandbox

## Purpose (WHY)
A sandbox for testing the Claude + GitHub Action integration before applying patterns to production repos (Salescake CRM and Power Upgrade Solar). Used to verify workflow triggers, GitHub App auth, and Anatomy of a Claude Code Project conventions.

## Repo Map (WHAT)
- `index.html` — demo page used to test UI fixes
- `.github/workflows/claude.yml` — workflow that triggers Claude on @claude mentions in issues / PRs
- `.claude/skills/` — reusable expert workflows (code review, etc.)
- `.claude/hooks/` — deterministic guardrails (formatters, blocked dirs)
- `docs/architecture.md` — system overview
- `docs/decisions/` — Architecture Decision Records (ADRs), numbered 0001-, 0002-, ...
- `docs/runbooks/` — operational runbooks
- `CLAUDE.md` — this file (repo memory / north star)

## Rules (what's allowed / not allowed)
- HTML/CSS/JS: prefer vanilla and minimal dependencies
- Keep changes scoped to what was asked — no drive-by refactors
- Always open a pull request rather than committing to `main` directly
- For UI work: include a Playwright screenshot in the PR body
- Never commit secrets, API keys, or credentials
- Don't edit `.github/workflows/claude.yml` unless explicitly asked

## Workflows (how work gets done)
Tag `@claude` in any of:
- An issue body or title
- A PR comment
- A PR review or review comment

Claude will read the repo, do the work, and open a PR. UI work should include a screenshot in the issue.
