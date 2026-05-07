# Architecture

## Overview
This sandbox is intentionally minimal — one HTML page plus a CI workflow. The architecture exists to verify the Claude + GitHub integration end-to-end before applying patterns to production repos.

## Components
- **GitHub Action** (`.github/workflows/claude.yml`) — fires on `@claude` mentions, runs `anthropics/claude-code-action@v1`, authenticates via the org-level `ANTHROPIC_API_KEY` secret
- **Claude GitHub App** — installed at the `salescakecrm` org level, grants the workflow read/write access to repo content, issues, and PRs
- **Static HTML** (`index.html`) — minimal page used as the surface for UI test fixes

## Decisions
See `docs/decisions/` for architecture decisions (ADRs).
