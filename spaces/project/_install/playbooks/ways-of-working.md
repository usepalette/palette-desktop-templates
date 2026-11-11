---
type: playbook
owner: "[Owner]"
status: draft
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
read_when:
  - "You need to know how the team runs a project: its meetings, its channels, who decides and what done means"
  - "You are planning the first weeks of a project"
---

# Ways of working

> **Not filled in yet.** Say "fill in how we run projects" and it gets written with you.
>
> 1. Ask how a project runs day to day: which meetings recur and what each is for, where the team and the people it works for talk, when people are available, who makes which calls, and what has to be true before work counts as done. Only habits that hold across projects belong here.
> 2. Write only what you are given. End a line you worked out yourself with "(to confirm)", and leave a slot you have nothing for in its brackets.
> 3. Delete this box when the page holds only what a person stated themselves, or when a person confirms it, and set `status: active`. Follow `.agents/page-states.md` at the workspace root.

How the team runs a project day to day, whichever project it is. A project that runs differently says so in its own `README.md`, and this page stays the default. The company's rituals and channels are in [`company/how-we-work.md`](../../../company/how-we-work.md) and its tools in [`company/tools.md`](../../../company/tools.md): this page links to them and never copies them.

## Cadence

| Ritual | When | Who | What it is for |
|---|---|---|---|
| [A meeting that recurs on a project, such as a standup, a check-in with the customer, a demo or a retro] | [how often, the day and the time] | [who attends] | [its purpose, in a line] |

A meeting that decides or changes something gets a note in the project's meetings folder: say "log this meeting".

## Communication

- **Where the project team talks:** [the channel each project gets, and how it is named]
- **Where we talk with the people the project is for:** [a shared channel, email or calls]
- **Status update:** [how often a written update goes out, where, and who writes it]
- **How fast we answer:** [the response the team commits to, and on which days]

## Availability

- **Time zones:** [where the team and the people it works with are]
- **Hours we overlap:** [the hours when everyone is reachable]
- **Time off:** [how it is announced. Anything that moves a date also goes in the project's timeline, `projects/<name>/timeline.md`, when it keeps one]

## How we decide

- **Who makes the calls:** [who decides what on a project: delivery, scope, design, and what needs the yes of the people it is for]
- **What gets written down:** every real decision gets a dated `Decision:` line in the project's `README.md`, and one with real options or consequences a numbered record: [`processes/record-a-decision.md`](../processes/record-a-decision.md).

## Definition of done

- [What has to be true before a piece of work counts as done: who reviews it, how it is checked, who sees it]
- [Work that needs an extra review, and whose review]
