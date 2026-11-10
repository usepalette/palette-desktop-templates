---
type: doc
owner: "[Owner]"
status: draft
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
read_when:
  - "You're deciding where a fact lives, or where to look something up"
  - "You're about to write a task, a customer record or a follow-up somewhere"
---

# Tools

> **Not filled in yet.** Say "help me fill in our tools" and it gets written with you.
>
> 1. Ask where each kind of fact lives, and check which tools you can reach yourself. Record local ownership when no external tool is used, especially the task fallback below; remove only irrelevant rows. Add a row for any other system that owns a kind of fact.
> 2. Write only what you are given. End a line you worked out yourself with "(to confirm)", and leave a slot you have nothing for in its brackets.
> 3. For drafted or inferred content, keep this box and change its first line to "**Not confirmed yet.**" Directly supplied facts need no second approval; use the root page-state procedure.
> 4. Delete this box when the page holds only what a person stated themselves, or when a person confirms it, alone or in a clearly named batch they have reviewed. Then set `status: active`. Follow `.agents/page-states.md` at the workspace root; preserve the owner, and leave brackets for what nobody knows yet.

Which system owns which fact. Each field has one authoritative home. This workspace may hold dated, linked summaries for context; they are snapshots, not live records. Read the source again before claiming a tool-owned value is current.

| Fact | Lives in | Notes |
|---|---|---|
| Tasks and issues | [the tracker, or company/tasks.md if no tracker is used] | One authoritative list; see below |
| Customer records and pipeline | [the tool, or customer briefs if no CRM is used] | Name which fields it owns; brief snapshots link to it with a checked date |
| Code | [the tool] | |
| Files and documents | [the tool] | |
| Conversations | [the tool] | |
| Meeting notes and transcripts | [the tool] | See [`meetings.md`](meetings.md) |
| Images, video and other heavy files | [the tool or shared folder] | Kept out of this workspace; link to them |
| Confidential material: pay, contracts, personnel, finance | [the restricted tool or folder, or "none yet"] | Never on a page the whole team reads; refer to it without the details |

## What this workspace owns

Stable company context, the reasoning behind decisions, the rules for working here, and the synthesis that doesn't fit in any tool's fields: what we actually think about a customer, why a project exists, how a team approaches its work.

When a summary repeats a tool-owned field, label its source and date checked. Do not maintain a second editable version or sync over human notes. Without a CRM, customer briefs may own relationship fields; record that choice above. When a tool is replaced, change its row and add a line to [`log.md`](log.md).

The Notes column is also where a tool's quirks go, once someone has run into them: how it behaves, what to check after writing to it. A tool the company has stopped using keeps its row, marked "retired, do not read", until nothing points to it any more.


## When there is no task tracker

If the team confirms it has no tracker, use one shared file, `company/tasks.md`, as the task home. Create it only when an actual task is requested, with full frontmatter (`type: doc`, known owner, `status: active`, date, acting person, `edit_policy: team`) and a table: Task, Owner, Due, Status, Context. Record only supplied owners and dates; mark unknowns clearly. Add its link to `company/README.md` when it exists, and set the Tasks row above to this file.

Project and customer briefs link to those task rows or the file instead of maintaining checklists. Meeting notes can keep the historical action with a link to its current task. A log records history, not open work.

If the task destination is unknown, ask once; keep captured follow-ups in the requested note while awaiting the answer. If a configured tracker is merely unreachable, leave explicitly unsent follow-ups in the note and say they were not filed; do not start a fallback tracker. Moving to a tracker later requires one deliberate migration and updates to this page and the old list.
