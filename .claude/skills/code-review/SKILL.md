# Code review skill

A reusable checklist Claude follows when reviewing PRs in this repo.

## When to use

When asked to review a PR, look at the diff and walk through this checklist before commenting.

## Checklist

**Scope.** Are the changes limited to what the issue asked for? Flag any drive-by refactors.

**Naming.** Are new variables, functions, files named clearly and consistently with surrounding code?

**Tests.** If the change is non-trivial, is there a corresponding test or visual verification (e.g., Playwright screenshot for UI)?

**Secrets.** Are there any committed credentials, API keys, or .env contents? (Should be NONE.)

**Side effects.** Does the change touch shared state, global config, or migration files?

**Reversibility.** Could this change be safely reverted in one commit if it breaks production?

## Output format

Post a single PR review comment that contains a 1-line summary verdict (approve, request changes, or comment), a description of any issues found tagged with their line number or filename, and a short recommendation if approval is blocked.
