---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
cadence: ""
read_when:
  - "Someone asks for work to be reviewed or checked before it is shared"
  - "A piece is about to go out under the company's name or a person's"
---

# Review GTM work

A check of GTM work before it is shared, against the brand, the strategy and the state of the workspace. It produces a short list of what to fix, each with the page or the rule it breaks. Run it as a teammate reviewing, not a linter.

## When to run this

- Someone asks: "review this before I share it", "check this against our brand", "is this ready to go out?"
- Before a piece goes out under the company's name or a person's: a post, a page, a launch kit, a message to a customer
- After a session that changed the strategy, the positioning or a customer's folder

## Steps

1. **Understand the scope.** Ask what changed, or read the files changed in the session. Say what kind of work it was: a piece of content, a launch, a customer update, a change to the strategy or the positioning, or a change to this space.
2. **Pick the checks that apply** from **The checks** below. Most work needs two or three of them, not all seven.
3. **Run them,** and keep only the findings that pass **What to flag**.
4. **Show the findings** in the shape under **The output**. Change nothing on your own: a fix is made after the person's yes.
5. **Write back what repeats.** A finding the team has seen before is proposed as a line in this space's [`lessons.md`](../lessons.md), or as a change to the playbook or the format it comes from.

## What to flag

Ask three questions of each possible finding:

- **Would it cause a problem if it shipped?** A wrong date, a broken link, a stale status.
- **Would it confuse someone reading it later?** A file missing from its list, two pages that disagree.
- **Would it embarrass us in public?** Copy that is off the voice, the wrong positioning, a bracket left in.

If the answer to all three is no, don't flag it. Never flag a style preference that no page backs, a "could be stronger", a problem that was there before this work, or something imperfect but clearly on purpose.

## The checks

### A. Voice and messaging

**When:** the work holds anything external: a post, a page, a launch piece, a message to a customer. Skip it for internal pages.

Read [`company/brand/voice.md`](../../../company/brand/voice.md) and [`company/brand/messaging.md`](../../../company/brand/messaging.md) first, and the author's `people/<name>/tone-of-voice.md` for anything under a person's name.

- **The voice:** hype or corporate words, words the voice page avoids, vague claims with no specifics, adjectives where a strong verb should be, and feature soup: capabilities where the workflows and the outcomes should be. Run the self-check in [`playbooks/content.md`](../playbooks/content.md) → Before it goes out.
- **The messaging:** a line that contradicts the positioning, a claim the product can't back (the product's file in [`company/products/`](../../../company/products/README.md) and the proof points say what it can), or the relief before the problem.

For each finding, quote the line of the brand page it breaks.

### B. The space and its links

**When:** always.

- **Lists:** a file that was added, moved, renamed or deleted shows up as it is now in its folder's README, in this space's [`README.md`](../README.md), and in [`AGENTS.md`](../AGENTS.md) → Where to read for a task.
- **Links:** every relative link in the changed files resolves. If a file moved, search for links to its old path.

For the whole workspace, the workspace check goes wider: say "check the workspace".

### C. Placeholders

**When:** always for anything about to go out, and after setup or a change to the foundations or the company's pages.

- A bracket, a slot from a format, or a "(to confirm)" left in a piece that is about to go out
- A quote, a number or a customer's name with no source behind it
- A page this work filled in that still opens with its **Not filled in yet** box

Brackets on a workspace page are open questions, not errors. Tell the person what is missing and offer to fill it in; never invent a value.

### D. Customers

**When:** a customer's folder was added or changed. Skip it if there are none.

- A new customer's folder was copied whole from its mold, and has its row in [`customers/README.md`](../../../customers/README.md)
- After a meeting, the note is in the customer's meetings folder, and the brief's **Now** line and Activity line say what changed
- The contacts, the dates and the next steps are real, or visibly unknown

### E. Completeness

**When:** files or folders were created.

- A new project has its brief from the mold, with `space: gtm` when it is GTM work, and its row in [`projects/README.md`](../../../projects/README.md)
- A new playbook, format or research file is listed in its folder's README
- A piece made from a format has the format's sections, and traces back to its messaging brief when it belongs to a launch

### F. Staleness

**When:** the changed files hold dates, statuses or next steps.

- The dates are current, and no next step or follow-up date is already in the past
- The statuses say what actually happened

### G. Strategy and positioning

**When:** the work talks about the product, the positioning or the market.

- It fits [`foundations/gtm-strategy.md`](../foundations/gtm-strategy.md): the current phase, the audience, the channel
- Its framing of the competitors matches their files in [`company/market/competitors/`](../../../company/market/competitors/README.md)
- Its audience matches [`company/market/ideal-customer.md`](../../../company/market/ideal-customer.md)

Understand the intent before flagging a deliberate choice.

## The output

The findings grouped by check, skipping the checks that did not apply. Each finding gives the file, what is wrong (quoted when it is a line), and the page or the rule it breaks, linked. If everything is clean, say "No issues found."

## Done when

- Every check that applies has run, and the person has the findings, or "No issues found."
- Nothing was changed without the person's yes.
