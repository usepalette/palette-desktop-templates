---
name: resolve-pr-checks
description: Fetch and fix failing PR checks (CI, lint, type-check, build, tests). Use when iterating on a PR that has failing GitHub checks.
---

Resolve failing PR checks for the current branch.

## Setup

Get owner/repo: `gh repo view --json owner,name -q '"\(.owner.login)/\(.name)"'`

## Steps

1. **Fetch checks**: Run `gh pr checks` to get the status of all PR checks.

2. **Show overview**: Present a compact summary table:
   - Check name | Status (pass/fail/pending) | Link
   - Include the check URL for every check (from `gh pr checks` output)
   - Filter out "skipping" checks and deduplicate entries (gh pr checks can return duplicates)
   - Highlight only the failing checks

3. **Fetch failure details**: For each failing check, run `gh run view <run-id> --log-failed` to get the failure logs. Extract the run ID from the check details URL. For non-GitHub-Actions checks (e.g., Railway), note that logs aren't available via `gh` — include the external link instead.

4. **Fix failures**: Work through each failure:
   - Analyze the logs to identify the root cause
   - Make the necessary code fixes
   - After fixing all issues, run `/check` to verify locally before pushing

5. **Push fixes**: After all checks pass locally, commit and push. Use `gt submit --stack --no-edit` if the branch is part of a Graphite stack, otherwise `git push`.

If a check is flaky or unrelated to our changes (e.g., infrastructure issue), note it in the overview and skip it.
