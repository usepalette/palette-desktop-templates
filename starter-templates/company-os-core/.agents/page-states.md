---
type: doc
owner: Shared
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: everyone
---

# Page states

How to distinguish instructions, unknowns, drafts and confirmed content.

## The visible marks

- **Not filled in yet:** the page has unknown slots. Real text already supplied on it is still usable; update a stale box to **Not confirmed yet** when drafting.
- **Not confirmed yet:** content has been drafted and still needs review.
- **Mold / Starter format:** reusable structure, never a real record. Copy it; don't fill the original.
- **Brackets:** unknown fields or reusable slots, never evidence. **None yet** is an empty collection.
- **No box:** a normal working page. Navigation, procedures and empty memory files work from day one; absence of a box alone does not prove a person reviewed every word.

## Draft and confirm

1. Follow the destination's README and copy its mold when available. Stamp the copy and replace its mold box with **Not confirmed yet** when the content still needs review.
2. A person's directly stated facts, answers or exact requested correction are already confirmed. Do not ask them to approve the same statement twice. A page that holds only what the person stated themselves, with no line you inferred or reworded, has nothing left to confirm: remove its box. A page that also holds a line of yours keeps **Not confirmed yet** until they have seen it. Permission to draft, or approval of a destination, does not confirm the agent's later wording.
3. Show the content, or provide the files for review, naming exactly what is ready. The person may confirm one page or a named batch. Never treat "go ahead" with work as approval of drafts they have not seen.
4. On confirmation remove the review box, remove the "(to confirm)" marks the person accepted, and set `status: active` on an ordinary page. Keep the existing owner unless reassignment was requested. A confirmed page may keep brackets: they are open questions, not errors, and no slot has to be filled before a page can be confirmed. Remove an unused section only when it adds no value. Reusable formats keep their slots.
5. A material new draft on a previously confirmed page restores a review box identifying the changed section; it does not erase approval of the rest. Typos, direct factual corrections and navigation updates need no new confirmation.

## Lifecycle is separate

For ordinary descriptive documents, use `draft` while drafting and `active` once confirmed. Navigation, procedures and empty memory files are `active` from creation.

For records with a defined lifecycle, follow their collection's schema: a project can be `draft` because it is exploratory even though its brief is confirmed, or `active` while a newly drafted section needs review. Customer lifecycle stage is its own field. Never change business state merely to remove a review box.

Do not mistake intentional blanks in a thin profile or slots in a confirmed reusable format for broken frontmatter. Placeholder dates and authors in untouched seed files are intentional; real workspace edits are stamped.
