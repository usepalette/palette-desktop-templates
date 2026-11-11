---
type: doc
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
read_when:
  - Someone asks for a design to be reviewed, critiqued or checked against the guidance
  - A UI change is about to ship
---

# Reviews

A review turns the team's guidance on one design: a branch, a preview, a design file, a screenshot or a shipped screen. The output is a short ranked list of things to improve. Then whatever the review settled is written back, so the next session starts from it instead of arguing it again.

## Read the guidance first

In this order, before looking at the design.

1. **The rules** — The area files in [`../rules/`](../rules/README.md) the design touches. A design that breaks one is breaking a decision the team already made
2. **The principles** — The pages in [`../principles/`](../principles/README.md) the design touches. Anything on top of anything else means `layering.md`; anything with words means `writing-in-the-product.md`
3. **The design system** — The component and foundation pages for what the design uses, and the code they point to

## Look at the real thing

Open the running branch, the preview or the design file at its real size, in its real context. A part shown alone, or at a size the person never sees, misleads.

## Review in one order

Go from the largest decision to the smallest: the job of the screen, then structure and depth, then layering, then grouping and spacing, then components and tokens, then type, then words, then states.

Keep the two kinds of finding apart.

- **From a rule** — The design breaks a settled call. Name the rule file and the rule
- **From judgment** — The design could be better by a principle. Name the principle

## The output

A ranked list, most important first. Each line says where it is and what to change, in plain language, and whether it comes from a rule or from judgment. No essays, and no design vocabulary standing in for a point. Check the design against every rule in the area files it touches, and report each one it breaks.

## Reviewing as a team

A crit, a design review meeting or feedback in a channel works the same way. The agent can take the notes or the recording and do the write-back.

- **Before** — The designer shares the running branch or the design file, and the agent's ranked list, so the team spends its time on the calls that are still open
- **During** — The team decides what the rules do not settle yet
- **After** — The notes go in the draft's folder as a dated file named for what was reviewed, and every call made becomes a proposed rule

## Write back what it settled

A review that settles nothing gets repeated next month.

- **A new call** — Propose it as a rule in its area file. Write it after a yes
- **A correction** — The nearest `lessons.md`
- **What happened** — A line in the nearest `log.md`: the project's, or the space's

A review proposes. What it settles goes to the person who owns the design as a proposal, never written into the rules as though it were already decided.
