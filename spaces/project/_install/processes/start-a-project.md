---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
cadence: ""
---

# Start a project

A new project in `projects/<name>/`, made the way the workspace makes every project, with the extras this team's projects use and `space: project` in its frontmatter.

## When to run this

- Someone says "we're starting a new project", or "set up the project for [a customer]", for a project this team runs.
- A project already in [`projects/`](../../../projects/README.md) should get the extras: set `space: project` in its frontmatter if `space` is empty, then start at step 4.

## The extras

**A new project here gets [the extras this team chose in setup] by default.** Setup fills in this line. Until it is filled in, ask which extras the project needs, in the same round as the other questions.

| Extra | Format | The copy goes to | What it adds to the project's `README.md` |
|---|---|---|---|
| A fuller brief | [`templates/brief.md`](../templates/brief.md) | `projects/<name>/brief.md` | the background, the problem, the audience, what success looks like and the constraints |
| Goals with metrics | [`templates/goals.md`](../templates/goals.md) | `projects/<name>/goals.md` | the outcomes, the non-goals, and each metric with its baseline and target |
| A stakeholder map | [`templates/stakeholders.md`](../templates/stakeholders.md) | `projects/<name>/stakeholders.md` | how much each person can change the project, how much it changes their work, and how they are kept involved |
| Scope with a change log | [`templates/scope.md`](../templates/scope.md) | `projects/<name>/scope.md` | the full in and out lists, the assumptions, and every change since the scope was agreed |
| Phases | [`templates/timeline.md`](../templates/timeline.md) | `projects/<name>/timeline.md` | the phases with their dates, the dates the plan must respect, and the risks to them |

The other formats in [`templates/`](../templates/README.md) are copied when their first page is needed: a glossary when the project has words of its own, a decision record with the first real decision, an interview or the findings with the first research, the design links with the first design file.

## Steps

1. **Take what you were given.** A name and one line on what the project is for are enough to start; the owner, the dates, the customer and the people are written when they are known. Anything the person said earlier counts. Ask only for what is still missing, in one round, including who the project is for and, while the line above is not filled in, which extras it needs.
2. **Check the customer.** A project for a customer links to the customer's folder in [`customers/`](../../../customers/README.md). If they have none yet, offer to add it first, following [`customers/README.md`](../../../customers/README.md) → Add a customer, after a yes. Without one, `customer` stays empty and who the project is for goes under Open questions in the project's `README.md`.
3. **Make the project the workspace's way.** Follow [`projects/README.md`](../../../projects/README.md) → Start a project, as written: it checks the project doesn't exist yet, copies the mold, writes only what you were given, stamps the frontmatter, adds the row and links the customer. In the frontmatter, `space` is `project`. Those steps live there; this page never repeats them.
4. **Add the extras.** For each extra the project gets, copy its format, from **Fill in** down, to where the table above says, with its own full frontmatter: `type: doc`, the project's owner and edit policy, `status: draft`, today and the person you are working for. Fill only what you were given, by the person or by a document they hand you, such as a statement of work or kickoff notes; a slot you have nothing for keeps its brackets. Material from a document follows the root rules for bringing material in: show where each piece would go and write after a yes. A page drafted from it carries a **Not confirmed yet** box until a person has read it, following `.agents/page-states.md` at the workspace root.
5. **Keep one home per fact.** The project's `README.md` stays the summary: the Now line, the milestones, the people and the decisions live there and nowhere else. Add a row for each extra to its Links table. When the project has a scope page, the README's Scope section keeps one line each for in and out and links to it. In the People table, a teammate's name links to their profile in [`people/`](../../../people/README.md), and a customer's person is one of the customer's key people, added there first when they are not yet. The stakeholder map adds influence and interest to those people, never a second roster.
6. **Leave the rest for later.** The project's decisions, research and design folders are made when their first file arrives, never empty: [`templates/README.md`](../templates/README.md) → Folders a project makes later. Tasks stay in the task home named in [`company/tools.md`](../../../company/tools.md), and the project's `tracker` field links to them.
7. **Say what you made**, and what is still blank. Offer one next step, such as logging the kickoff meeting or filling in the stakeholder map.

## Done when

- The project is in `projects/<name>/`, made the workspace's way, with `space: project`, its row in the Active table of [`projects/README.md`](../../../projects/README.md), and the link both ways to its customer when it has one.
- Each extra it uses is in its folder with its own frontmatter, linked from its `README.md`, and holds nothing that wasn't given.
