---
type: index
owner: Shared
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: everyone
---

# Commands

The flows people ask for again and again, one page each. Each page is a short procedure, and most of them point to the steps on a folder's own `README.md`, so the steps live in one place.

Nobody has to name a command. People say what they want ("check the workspace", "add a colleague", "log this meeting") and the agent follows the matching page. Where the app shows a command menu, the same pages appear there by name.

| Command | Say | What it does |
|---|---|---|
| [`new-person`](new-person.md) | "Add a colleague" | Adds a person: folder, profile and roster row |
| [`create-space`](create-space.md) | "We need a space for product" | Makes a space for an area of work: a team, a discipline or a body of work |
| [`new-customer`](new-customer.md) | "We just signed a new customer" | Adds a customer, client or account |
| [`new-project`](new-project.md) | "We're starting a new project" | Starts a project |
| [`close-project`](close-project.md) | "That project is done" | Closes a project and records how it ended |
| [`new-meeting`](new-meeting.md) | "Log this meeting" | Writes the meeting note where it belongs and updates what the meeting changed |
| [`add-playbook`](add-playbook.md) | "Let me explain how we do this" | Captures how a piece of work is done, in the space it belongs to |
| [`import`](import.md) | "I want to bring in what I already have" | Brings in documents, connected tools or what another AI tool knows, with a proposal first |
| [`workspace-heal`](workspace-heal.md) | "Check the workspace", "is anything broken?" | Looks for broken links, lists that no longer match their folders, pages nobody has confirmed, scratchpads that have piled up. Reports first; fixes the safe things when asked |
| [`reflect`](reflect.md) | "Tidy the lessons" | Goes through the `lessons.md` and `log.md` files and proposes what to merge, move, promote into a guide or drop. Suggests only |
| [`finish-session`](finish-session.md) | "Let's wrap up" | Ends a session worth revisiting: what was done, what is left, and the memory lines |

## They adapt to the workspace

Every command works with what it is given, asks only for what is missing, and follows the workspace as it is today. A company that renamed a folder, removed one it doesn't need or added its own keeps using the same commands: the map in the root `README.md` says where things live, and the page a command points to always wins over the command itself.

## Adding a command

1. Add a file here with `type: command`, a one-line `description` and, if it takes input, an `argument-hint` in its frontmatter. Add a row in the table above.
2. Keep the steps in one place. If a folder's `README.md` already holds them, the command points there instead of repeating them.
3. A flow that belongs to one area of work goes in that space's `processes/`. How a command page is stamped and named is in [`../conventions.md`](../conventions.md).
4. **Make it show up in the command menu.** Each page here has a small pointer file with the same name in `.claude/commands/` at the workspace root, for hosts that read commands from there. The pointer carries only the same `description` and `argument-hint` and names the page here; the procedure is never copied into it. Add one when you add a command, and remove it when you remove one. If the pointer can't be removed from inside a session, say so, so the person can remove it.
