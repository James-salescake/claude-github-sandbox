# Project context for Claude

This repo is a sandbox for testing the Claude + GitHub integration described in James's setup transcript.

## What this repo is for
- Verifying the `claude-code-action` workflow fires on `@claude` mentions
- Exercising the Playwright MCP (browser automation) inside CI
- A safe place to break things before wiring this into production repos (Salescake CRM, Power Upgrade Solar)

## How to invoke Claude
Tag `@claude` in any of:
- An issue body or title
- A PR comment
- A PR review or review comment

Claude will spin up the workflow, read the repo, and do the work. UI work should include a screenshot — Claude can see images in issues.

## Coding style
- HTML/CSS/JS: prefer vanilla and minimal dependencies for this sandbox
- Keep changes scoped to what was asked — no drive-by refactors
- Always open a pull request rather than committing to `main` directly

## Files Claude should know about
- `.github/workflows/claude.yml` — the workflow that triggers Claude. Do not edit unless explicitly asked
- `index.html` — the demo page used to test UI fixes. Edit this freely
- `CLAUDE.md` — this file. Update it as the project grows so Claude always has fresh context

## Tools Claude has in CI
- File read/write inside the repo
- Bash limited to: `npm install`, `npm run build`, `npm test`, `npx playwright test`
- Playwright MCP — a real headless Chromium browser. Use it to verify UI changes by navigating to the site and taking a screenshot before opening the PR

## When opening a PR
- Title should describe the change in one line
- Body should include: what changed, why, and (for UI work) a Playwright screenshot of the result
- Link the issue with `Closes #N`
