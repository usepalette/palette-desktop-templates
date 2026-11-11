---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
cadence: ""
---

# Record a decision

A numbered record of a decision on a project, with its context, its options and its consequences, and the dated `Decision:` line in the project's `README.md` that links to it.

## When to run this

- Someone says "we decided …", "record this decision" or "the scope changed", about a project.
- A meeting note, a thread or a review settles something that answers "why did we do it that way?": a trade-off between real options, a change of scope or priority, a direction with consequences, or a change of mind on an earlier decision.
- A decision recorded earlier as proposed is now made: step 3 accepts that record instead of writing a new one.

A small choice needs only its dated `Decision:` line in the project's `README.md`, or a line in the meeting note. A decision about how the team runs projects in general is a `Decision:` line in this space's [`log.md`](../log.md), not a record.

## Steps

1. **Find the project.** The decision belongs to one project in [`projects/`](../../../projects/README.md); ask which if it is not clear.
2. **Take the facts from the person or the material.** What was decided, when, by whom, the context, the options, why, and what follows. Write only what you were given; a section you have nothing for keeps its brackets. A suggestion is never written up as a decision: if it is not decided yet, the record is proposed.
3. **Accept a proposed record; never write a second one.** Look in `projects/<name>/decisions/` for a proposed record of the same decision: `status: draft`, with its Status line proposed. When there is one and the decision is now made, it keeps its number and its file. Set its `status: active` and its Status line to accepted, add what changed since it was proposed, and change its Status in the folder's `README.md`. In the project's `README.md`, its line under Open questions becomes a dated `Decision:` line that links to it, in the format of step 7. Then update what it changed (step 8) and say what you wrote (step 9). Skip steps 4 to 7.
4. **Number it.** Look in `projects/<name>/decisions/`: the next number is the highest there plus one, in four digits, `0001` for the first. Never reuse a number or write over a record: if the file appeared while you worked, take the next number.
5. **Make the folder on first use.** A project without a decisions folder gets one now, with its own `README.md`: [`templates/README.md`](../templates/README.md) → Folders a project makes later.
6. **Write the record** as `projects/<name>/decisions/NNNN-<slug>.md`, the slug in kebab-case from its title, from [`templates/decision-record.md`](../templates/decision-record.md): everything from **Fill in** down, with the frontmatter that format names. Add its row to the table in the folder's `README.md`.
7. **Add the `Decision:` line** to the **Decisions** section of the project's `README.md`, newest on top: `**YYYY-MM-DD** — Decision: [what was decided, in one line]. [NNNN](decisions/NNNN-<slug>.md)`. If a meeting note already put the line there, add the link to that line instead of writing a second one. A proposed decision gets no `Decision:` line yet: it goes under Open questions, with the link, and gets its line once it is accepted, through step 3.
8. **Update what it changed.** A change of scope changes the in and out lists, and gets a dated row in the change log of the project's scope page when it keeps one, linking the record. A milestone that moved changes in the Milestones table. A record that this one supersedes changes only its frontmatter and its Status line, as its format says, and its row in the folder's `README.md` says it was superseded. Refresh the **Now** line if the next step changed.
9. **Say what you wrote**: the record, or the proposed record you accepted, the line in the project's `README.md`, and anything else you updated.

## Done when

- The record is in `projects/<name>/decisions/`, numbered, and listed in that folder's `README.md`. A decision that was proposed earlier is the same record, now accepted: never a second one.
- The project's `README.md` has a dated `Decision:` line that links to the record, or, for a proposed decision, a line under Open questions.
- The scope, the milestones and any superseded record say what the decision changed.
