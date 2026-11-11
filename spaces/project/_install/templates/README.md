---
type: index
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
---

# Templates — Project

Reusable **fill-in formats** for the pages a project makes again and again: the modular partner to [`playbooks/`](../playbooks/README.md). A playbook says how the team works; a template gives the exact format to fill in. Read the playbook to decide, then copy the template to produce.

Codify a repeatable page once as a template, and every future one comes out consistent: same structure, same quality bar, no reinventing.

## How templates work

- **The template is the source of truth for shape.** Extend it and every new project inherits the change. Pages already copied keep their own shape.
- **They compose with the context.** A template says which pages to load first (the project's `README.md`, the customer's brief, the company's glossary), so a copy stays consistent without repeating the rules in every file.
- **Copy, don't edit in place.** Copy the format under **Fill in** to where the work lives, a project folder, then fill it in. The copy needs its own full frontmatter, with the fitting type, owner, status, date, acting person and edit policy; follow `.agents/page-states.md` at the workspace root. The original template's brackets stay.

**This space's, or everyone's?** A format the whole company uses belongs in the company's shared [`templates/`](../../../company/templates/README.md), not here.

## Templates

| Template | Use it for | The copy goes to |
|---|---|---|
| [`brief.md`](brief.md) | A project's full brief: the background, the problem, the audience, what success looks like, the constraints | `projects/<name>/brief.md` |
| [`goals.md`](goals.md) | The outcomes, the non-goals and the metrics, each with a baseline and a target | `projects/<name>/goals.md` |
| [`stakeholders.md`](stakeholders.md) | The stakeholder map: influence and interest for the people in the project's People table | `projects/<name>/stakeholders.md` |
| [`scope.md`](scope.md) | What is in and out, the assumptions, and the change log | `projects/<name>/scope.md` |
| [`timeline.md`](timeline.md) | The phases with their dates, the key dates and the risks to the timeline | `projects/<name>/timeline.md` |
| [`glossary.md`](glossary.md) | The project's own words, when it has many | `projects/<name>/glossary.md` |
| [`decision-record.md`](decision-record.md) | One decision with its context, its options and its consequences | `projects/<name>/decisions/NNNN-<slug>.md` |
| [`research-interview.md`](research-interview.md) | The notes from one interview | `projects/<name>/research/YYYY-MM-DD-<participant>.md` |
| [`research-findings.md`](research-findings.md) | What the project's research adds up to, kept current | `projects/<name>/research/findings.md` |
| [`design-links.md`](design-links.md) | Where the project's design files and prototypes are | `projects/<name>/design/design-links.md` |

The first five are the extras a project can start with, in [`../processes/start-a-project.md`](../processes/start-a-project.md). The others are copied when their first page is needed. Copy [`_template.md`](_template.md) when the next format is written, and list it here.

## Folders a project makes later

A project starts with its `README.md` and its meetings folder. These three folders are made in the project when their first file arrives, never empty:

- **`projects/<name>/decisions/`**, with the first decision record. Its `README.md` is headed "Decisions — [Project name]", says in one line that it holds the project's numbered decision records and that a record is never rewritten, and has a table: #, Decision, Date, Status.
- **`projects/<name>/research/`**, with the first interview or the findings. Its `README.md` is headed "Research — [Project name]", says in one line that it holds the interviews and what they add up to, with first names or pseudonyms only and recordings linked where they were made, and has a table: File, What, Date.
- **`projects/<name>/design/`**, with the design links. Its `README.md` is headed "Design — [Project name]", says in one line that it holds the links to the design files and prototypes and the reasoning they can't hold, while the files stay in the design tool, and has a table: File, What.

Each of these `README.md` files carries the full frontmatter: `type: index`, the project's owner and edit policy, `status: active`, today and the person you are working for. Add a row for the folder to the Links table of the project's `README.md`.
