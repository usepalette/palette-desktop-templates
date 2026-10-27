---
type: index
---

# Drafts — [Full Name]

My explorations, one folder each. The work itself happens in a design file or on a branch of the repo; the folder here says what I am exploring, where the work is and what I learned. Everything here is a proposal. The rest of the team can read it, and agents search it before starting similar work.

## Current drafts

| Draft | What it is | Status | Design file, branch or PR |
|---|---|---|---|
| _None yet._ | | | |

Status is one of: exploring, in review, shipped, dropped.

## Start a draft

1. **Make a folder named for the subject**: `drafts/<subject>/`, for example `drafts/settings-navigation/`. The subject is the thing a teammate would recognise, not the round of work.
2. **Give it a `README.md`** with frontmatter (`type: doc`), and say:
   - **What** — what you are exploring and why
   - **Status** — exploring, in review, shipped or dropped
   - **Where** — the design file and page, or the repo, the branch and the pull request once there is one
   - **What I learned** — what the next person should know, filled in as you go
3. **Add a row** to the table above.

## Keep it usable

- **One file page or one branch per draft.** Improve it in place. No `-v2` copies.
- **Start from what ships.** A draft builds on the real components, in the library or in the code, never on a copy drawn from scratch.
- **When a draft settles something, write it down.** A settled call becomes a rule in `rules/`, a correction into the nearest `lessons.md`. The draft's "What I learned" points to them.
- **When a draft grows into shared work,** a second person joins or it gets a deadline of its own, propose a `projects/` folder for it at the root and leave a line here pointing to it.
- **Shipped and dropped drafts stay** with their status and what was learned, so nobody explores the same thing twice. Delete one only when it taught nothing.
