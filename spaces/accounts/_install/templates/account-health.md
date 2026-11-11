---
type: template
owner: "[Owner]"
status: draft
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
read_when:
  - "You're adding or updating the Health section of a customer's brief"
---

# Account health

> **Mold.** Copy the part under **Fill in** into a customer's brief, `customers/<name>/README.md`, as its **Health** section, after **Plan** when the brief has one, otherwise after **What they care about**; don't fill it in here.
>
> In the copy: write a signal only from a source you read, with the source and the date you checked it. A signal nobody could read stays Unknown; never fill one from a guess. Replace the section at the next read: it is a snapshot, not a history. The section takes no frontmatter of its own: stamp the brief's `last_updated` and `last_updated_by`.

How an account is doing, read from the signals that show it. It sits in the customer's brief, and [`../processes/read-account-health.md`](../processes/read-account-health.md) keeps it current.

## How to write this

- **Load first:** the brief's **Activity** and its latest meeting notes, then [`company/tools.md`](../../../company/tools.md) for the tool that owns usage, contacts and stage.
- **Length and shape:** the status, the table and the flag. Context stays in the meeting notes.
- **Quality bar:** every value says where it comes from and when it was checked. A section that reads well but rests on a guess is worse than one that says Unknown.
- **The values:**
  - **Product usage:** Active, Inactive or Unknown
  - **Communication:** Recent (a touch within the rhythm the account usually has), Stale (longer than that, or a follow-up we owe is overdue) or None
  - **Engagement:** High, Medium or Low, from who comes to the calls, how fast they answer and whether they do what they said
  - **Status:** Healthy, Watch or At risk, read from the three signals together
- **The flag** says what needs attention, including a stage the signals contradict, such as Active with communication None.

## Fill in

_Copy from here down into the brief._

## Health

**Status:** [Healthy / Watch / At risk], read on [YYYY-MM-DD]

| Signal | Value | Source | Checked |
|---|---|---|---|
| Product usage | [Active / Inactive / Unknown] | [the analytics tool named in company/tools.md, or who said it and where] | [YYYY-MM-DD] |
| Communication | [Recent / Stale / None] | [Activity, the latest meeting note, or the email or chat tool] | [YYYY-MM-DD] |
| Engagement | [High / Medium / Low] | [the meeting notes and Activity] | [YYYY-MM-DD] |

**Flag:** [What needs attention and why, in a line or two, or "Nothing"]
