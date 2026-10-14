---
type: doc
owner: "[Owner]"
status: draft
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
read_when:
  - "You're logging, preparing or summarising a meeting"
---

# Meetings

> **Not filled in yet.** The four settings below are asked once, the first time someone logs a meeting, and written here so nobody is asked twice.
>
> 1. When the first meeting is logged, write the note first, with the safest choices (summary only, follow-ups kept in the note, no transcript stored). Then ask the four questions in one round. If the person would rather not answer, write "not decided" in the slots, so nobody is asked again.
> 2. Everything under "Where a meeting note goes" and "Rules for every note" applies from day one.
> 3. Direct answers are confirmed facts. If you draft or infer settings instead, change this box to "**Not confirmed yet.**"
> 4. Remove the box once the settings are confirmed, alone or in a named batch. Follow the root page-state procedure; preserve unknown optional settings.

How the company notes its meetings, and where a note goes.

## Settings

- **Notes come from:** [the notetaker or recorder in use, or written by hand]
- **Transcripts:** [kept in full at the bottom of the note, summary only, or never stored]
- **Follow-ups go to:** [the task home named in `tools.md`, or the meeting note only]
- **Never written down:** [what stays out of meeting notes]

## Where a meeting note goes

A meeting becomes one note, `YYYY-MM-DD-topic.md`, written from the `_template.md` in the `meetings/` folder it belongs to. It works from whatever the person has: pasted notes, a transcript, a recorder's summary or a spoken recap.

| The meeting was about… | The note goes in | Also update |
|---|---|---|
| A project | `projects/<project>/meetings/` | the project README: a `Decision:` line per real decision, milestones or health that changed, the Now line |
| A customer, no project | `customers/<customer>/meetings/` | the customer README: one dated Activity line linking the note, the Now line, any section the meeting changed |
| A project for a customer | `projects/<project>/meetings/` | both of the above; the customer's Activity line links to the project's note |
| The work in a space (a team meeting, a planning session, a review) | `spaces/<space>/meetings/` | the space's `log.md` for decisions. On first use copy both files from [the shared meeting mold](../.agents/meeting-template/README.md), then fill the README's context, known owner, edit policy, date and attribution |
| The company as a whole, or no single space (an all-hands, a leadership meeting) | `company/meetings/`. On first use copy both files from [the shared meeting mold](../.agents/meeting-template/README.md) and add the folder to `company/README.md` | a `Decision:` line per real decision in the root `log.md` |
| Something with no folder yet | offer the relevant customer or project folder only if useful; if declined, save in the person's `scratchpad/` using the shared meeting mold | a `Decision:` line per real decision in the nearest fitting `log.md` |

For a scratchpad note, copy only the shared `_template.md`, stamp it, add it to the scratchpad index and leave the mold unchanged. It is an intentional exception to the usual `meetings/` location; don't create a business record the person declined.

## Rules for every note

- **The date is never assumed to be today.** The date, the attendees and the kind of meeting come from the material; only what is missing is asked for.
- **One note per meeting.** Check whether the meeting already has a note before writing a new one.
- **Work from the transcript when there is one,** not from a generated summary: summaries put action items on the wrong person.
- **Attribute carefully.** A name goes on a statement only when the material makes clear who said it. Speaker labels from a recorder are unreliable. A suggestion is never written up as a decision.
- **The note is the record; the README is the synthesis.** The note is not pasted into the README. Nothing is invented: a section with no material is removed from the note, not filled.
- **One meeting, one note.** A meeting that covered two customers gets one note in the folder it was mainly about, and an Activity line in the other.
- **Follow-ups** follow the settings and the single task home in [`tools.md`](tools.md). A note may retain the historical action, with a link once filed. If a tracker cannot be reached, mark the action unsent and keep it in the note; don't claim it was filed. Choosing note-only capture records what was agreed, without establishing a competing live task list.
