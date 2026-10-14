---
type: index
owner: Shared
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
---

# Customers

One folder per customer you are actively engaged with. This is the **synthesis layer** on top of your CRM (the records, the pipeline), your product analytics (usage) and wherever conversations happen (chat, email, calls).

What goes here is what doesn't fit in a CRM field: what you actually think about a customer, the story of the relationship, what they care about, meeting takeaways.

If you call them clients or accounts, change the heading and the wording on this page. The folder itself stays `customers/`, because links across the workspace point at it.

## You need to…

| You need to… | Go to |
|---|---|
| Add a customer | Say "we just signed a new customer"; the steps are under **Add a customer** |
| Understand one customer fast | that customer's `README.md`: the **Now** line and the Story |
| Log a meeting | Say "here are my notes from the call"; the note goes in `<customer>/meetings/` and the brief is updated |
| Prepare for a call | the customer's `README.md`, then the last two meeting notes |
| See the projects we run for a customer | the **Projects** section of their `README.md`, which links into [`projects/`](../projects/README.md) |
| See where every customer stands | the table below, or the CRM's own views if you keep one |
| Know who we want as a customer | [`company/market/ideal-customer.md`](../company/market/ideal-customer.md) |
| Record a correction about how this folder works | [`lessons.md`](lessons.md) |

## When to create a folder

Create a folder when there is real engagement: meetings have happened, a shared channel exists, or they have signed. A name in the CRM doesn't need a folder. If you don't have enough context to write anything meaningful, you don't need one yet.

## The customer folder

Copied from [`_template/`](_template/README.md):

```
<customer>/
├── README.md     # the brief: who they are, Now, key people, what they care about, story, projects, links
└── meetings/     # one file per meeting: summary, key points, decisions, follow-ups
```

**Each field has one authoritative home.** Where a CRM owns contacts and stage, or analytics owns usage, the brief links to the source; useful snapshots include a source and checked date. Without a CRM, the brief may own the relationship fields. Set that choice in [`company/tools.md`](../company/tools.md). Keep confidential commercial details in an approved restricted source, never broad navigation.

## Add a customer

1. **Check they don't exist.** If `customers/<name>/` exists, or any `customers/*/README.md` already carries this `domain:`, open that folder instead.
2. **Copy [`_template/`](_template/README.md)** to `customers/<name>/`, whole: the `README.md` and `meetings/` with its two files. Name the folder with a short kebab-case label: the name people say, not the full legal name.
3. **Write only what you were given**, by the person, the CRM or a live connector. A line you worked out yourself ends with "(to confirm)", and a slot you have nothing for keeps its bracket, so the next reader can see it is unknown. Never invent people, numbers or history.
4. **Fill and stamp the whole copy.** Fill the customer's name and known owner in both the brief and `meetings/README.md`; set today's `last_updated`, the acting person's `last_updated_by` and the chosen edit policy in these real pages. Preserve `meetings/_template.md` as a mold. Fill known `domain`, `stage` and source fields without guessing. Use `status: active` for a live customer folder. Follow [page states](../.agents/page-states.md): drafts from sources keep a review box; directly stated facts need no second approval.
5. **Add the row** to the table below, replacing the "None yet" row if it is the first.

## Customers

| Customer | Stage / source checked | Owner | Updated | Now |
|---|---|---|---|---|
| _None yet._ | | | | |

## Conventions

- The `domain` field is a join key to the CRM when both exist. Never treat an unknown placeholder domain as an identity match. For a tool-owned `stage`, fill `source` and `source_checked` on the brief when actually checked; show that checked date beside the stage in the list.
- One dated line per meeting in the brief's Activity feed, newest on top, linking to the meeting file. Prefix genuine forks with `Decision:`.
- A brief grows with the relationship. Add a section when there is something real to put in it: what we are trying to achieve with them, their tools and how they work, risks.
- A customer that goes quiet keeps its folder; set `status: archived` in the README and move its row to the bottom of the table.
