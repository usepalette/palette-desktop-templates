---
type: index
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
---

# Discovery

Open questions, each with a plan to learn the answer. Discovery sits between interesting signal and the thesis in [`../strategy/`](../strategy/README.md) or the spec in [`../specs/`](../specs/README.md) that the evidence will justify.

Open a discovery file when the question matters and the answer isn't known yet. A clearly scoped request belongs in [`../user-feedback/feature-requests/`](../user-feedback/feature-requests/README.md), and a meeting note where [`company/meetings.md`](../../../company/meetings.md) puts it, not here.

## Lifecycle

`status` in each file says where the question stands:

- `open`: worth exploring
- `in-flight`: being researched now
- `promoted`: became a spec or a strategy thesis; link the outcome
- `closed`: answered with nothing further to do; say why

## Add a question

Copy [`_template.md`](_template.md) to a file named for the question's domain, in kebab-case, and set `status: open`. Frame the question, not a proposed answer.
