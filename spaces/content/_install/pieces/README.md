---
type: index
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
---

# Pieces

Every piece of writing the company ships, one file each, from the first draft to the link once it is out. This page lists them all: what is being written, what is waiting for someone to read it, and what went out where. Agents read it before starting a piece, so the same thing is not written twice.

## All pieces

Newest first.

| Date | Title | Channel | Status | Link |
|---|---|---|---|---|
| _None yet._ | | | | |

- **Date** is the day the piece was started until it goes out, then the day it went out.
- **Status** is `draft` while the piece is being written, `in-review` once its author says it is ready for someone else to read, and `published` once it is out. The piece's frontmatter says the same.
- **Link** is where the piece was published. A piece that went out before this space existed can have a row and no file.

## Add a piece

Say "help me write a post about…". [`processes/start-a-piece.md`](../processes/start-a-piece.md) copies [`_template.md`](_template.md) to `pieces/YYYY-MM-DD-<slug>.md`, with today's date and the working title in kebab-case, and adds its row at the top of the table. When the piece goes out, [`processes/publish-a-piece.md`](../processes/publish-a-piece.md) sets its status, date and link, here and in the piece.

## Keep it usable

- **One file per piece.** Improve it in place: no `-v2` or `-final` copies.
- **The row and the piece agree.** A change of status, date or link goes in both, in the same session.
- **A piece belongs to its owner.** Change its text for them, or with their yes.
- **Published pieces stay,** with their link, so the team can see what was said and where. The file keeps its name when the piece goes out, so no link to it breaks.
- **A piece that will not go out** is deleted with its owner's yes, and its row with it.
- **No heavy files.** Images and video stay in the tool named in [`company/tools.md`](../../../company/tools.md); the piece links to them.
