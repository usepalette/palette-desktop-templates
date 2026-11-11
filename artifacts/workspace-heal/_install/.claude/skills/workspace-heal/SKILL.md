---
name: workspace-heal
description: "Check a workspace for broken links, lists that no longer match their folders, unfinished or unconfirmed pages, missing furniture and drifting agent files, and fix the safe things when asked. Use when someone asks to check the workspace, asks whether anything is broken, wants broken links found or the safe things fixed, or runs /workspace-heal with report or fix. Reports first and changes nothing until asked to fix."
metadata:
  template: workspace-heal@2611111
---

# Workspace heal

Check the workspace against its own rules, say what has drifted, and fix the safe things when the person asks. Report mode is the default and changes nothing.

## 1. Pick the mode

- **Report**: "check the workspace", "is anything broken?", `/workspace-heal` or `/workspace-heal report`. Change nothing.
- **Fix**: "fix the safe things", "repair it", `/workspace-heal fix`. Apply only the safe fixes below, within what the person asked for.
- When the request could be either, report.
- A scheduled check reports only. Schedule one only when the person asks, with the timing, the destination and the scope agreed.

## 2. Learn the workspace's rules

The workspace's own rules are the standard. Read them before you check anything.

1. The root `AGENTS.md` and `README.md`. The README's map says where things live.
2. In a workspace made from Company OS Core (it has `.agents/conventions.md`): `.agents/conventions.md`, `.agents/page-states.md`, and `.agents/commands/workspace-heal.md` when it exists. That page is this workspace's own procedure for this check. Where it and this skill differ, it wins.
3. Before you check a folder, its `README.md`, and in a space its `AGENTS.md` too.
4. Note what the rules declare: frontmatter, page states, furniture, molds, indexes, commands, naming, generated files, where tasks live and where heavy files are stored (Core keeps both in `company/tools.md`).

Name the basis you used in the report:

- **Core**: the workspace follows Company OS Core's conventions. Run every check below.
- **Own rules**: the workspace has its own guidance. Run the checks its rules support, and the neutral ones.
- **None**: no usable guidance. Run only the neutral checks. Never call a file misplaced, a name wrong or a field missing without a rule that says so.

## 3. Map the workspace as it is

Never assume a folder name. A team may have renamed `customers/` to `clients/`, removed `projects/` or added a folder of its own. The map in the root `README.md` and the folders on disk say what is where, and the check follows them.

- **Collections** are folders whose `README.md` lists items made from a mold (`_template/` or `_template.md`): people, spaces, customers, projects, competitors, products, formats, meetings. Find them by their README and their mold, not by their name.
- **Spaces** are the folders the spaces index lists, and any folder with its own `AGENTS.md` beside a `README.md`.
- **Molds** are `_template/` folders and `_template.md` files. They are never real records and never count as items.
- **Host folders** (`.agents/`, `.claude/`, `.vibe/` and the like) are technical, not content.
- **Skip** `.git`, dependency folders, caches, build output and generated files the workspace does not treat as source. Don't follow links outside the workspace.

A map that disagrees with the disk is itself a finding, under **Lists and maps**.

## 4. Run the checks

Each finding names the path, what is wrong, the rule or the broken reference that makes it wrong, and whether it is a safe fix or needs a decision. Skip a check whose rule the workspace doesn't have. Collect the findings once, then report.

### Links

- Every real local Markdown link resolves, including heading anchors where they are used. Decode encoded paths before calling one missing.
- Skip web addresses, placeholder destinations, examples and links inside code. A backtick path with `<name>`, `[Space]` or `YYYY-MM-DD` in it is a pattern, not a link. A path the page says appears on first use, or only when another folder exists, is fine.
- Paths named in a `README.md` or an `AGENTS.md` exist.
- **Safe fix:** repair a destination only when the right one is unambiguous, such as a file that was renamed or moved. Otherwise show the choices. Never create a stub to make a link resolve.

### Lists and maps

- Each collection's index lists exactly its real items: no item without a row, no row without an item. Leave out molds and furniture (`README.md`, `AGENTS.md` and its pointers, `lessons.md`, `log.md`). An index does not list itself.
- The trees in the root `README.md`, and on `welcome.html` when the workspace has one, match the folders that are kept. Example names, on-first-use paths and a `SETUP.md` that setup has removed are not drift.
- When a folder was removed on purpose, its links and the procedures that used it (setup steps, meeting routing, commands) were changed too.
- **Safe fix:** add or remove a row that is clearly stale. Never guess a business status to fill a cell.

### Placement

- Working files sit in their folder, not in the workspace root. Meeting notes are where the workspace's meetings page says, or in the documented scratchpad fallback. Work with no clear home is flagged.
- A marked draft beside confirmed pages is fine. Heavy files follow the storage the workspace names.
- **Fix:** propose a move, unless the person already asked for it. Update the links in the same change.

### Page state and setup

- List the pages that are still **Not filled in yet**, the drafts still **Not confirmed yet** and the claims marked "(to confirm)". Keep optional completion apart from defects.
- Review and lifecycle are separate. A confirmed exploratory project can be `draft`. Navigation, procedures and empty memory files need no review box. Slots in molds and optional profile fields are intentional.
- When a `SETUP.md` exists, read it and check what it says is done. In Core, the root setup is done when the four core pages exist and are confirmed, and there is a first space or a clear decline of one; a missing required page is not finished setup. A space's own `SETUP.md`: say where that setup stands.
- **Fix:** never confirm content for the person. Offer a named batch for review.

### Frontmatter

- Every content Markdown file has frontmatter with a `type`. Folder READMEs and substantial pages carry the full block the conventions name. Small pages follow their mold.
- `AGENTS.md`, `CLAUDE.md`, `GEMINI.md` and other pointer files have none. An HTML page carries its block in the comment at its top.
- A real edit carries a date and the name of the person behind it, never an agent's. Untouched seed values (`YYYY-MM-DD`, `"[Owner]"`) and slots in molds are intentional. A value that starts with `[` is quoted.
- `template: <slug>@<version>` marks a page that Palette installed. Never remove or change it. Flag one that is malformed.
- **Safe fix:** add an obvious missing `type` or other known field within the scope asked for, and stamp what you changed with today's date and the acting person. Never invent an owner or a past date.

### Furniture

- The root, each top-level content folder, each space and each person have a `README.md`, a `lessons.md` and a `log.md`, where the conventions ask for them. A deeper folder needs a `README.md` and uses the nearest memory pair above it. Host folders need none.
- Every space has an `AGENTS.md`, and a `CLAUDE.md` and a `GEMINI.md` that point to it. Flag a space that is missing any of the three.
- A copy of a mold is complete: a customer or a project keeps its `meetings/` README and mold, with real headings and stamps. A collection of repeated items keeps its mold.
- **Fix:** flag an incomplete copy. Restore a missing piece only when asked, and keep what is there. Never invent local rules or facts.

### Memory

- Flag a `lessons.md` longer than about twenty entries, lessons that repeat or contradict each other, history in a lessons file, rules in a log, and relative dates such as "yesterday".
- Sensitive details don't belong in broad pages (`README.md`, `lessons.md`, `log.md`). Don't repeat them in the report.
- **Safe fix:** turn an unambiguous relative date into a date. Propose merging or promoting lessons the way the workspace's tidy-up flow does (`.agents/commands/reflect.md` in Core). Don't do it here.

### Scratchpads

- Each scratchpad's index matches its files. List older work for its owner to keep, promote or delete. Several versions, or links into a scratchpad from elsewhere, are signals to review, not proof that something should move.
- **Fix:** repair index rows within scope. Never move or delete another person's work.

### Commands and skills

- Each command page (in Core, `.agents/commands/`) has its row in the commands index, and a pointer with the same name in `.claude/commands/` that names it. Each pointer names a page that exists. The steps live in the page, never in the pointer.
- Each skill in `.claude/skills/<name>/`, `.agents/skills/<name>/` or `.vibe/skills/<name>/` has a `SKILL.md` with a `description` and a `name` that matches its folder.
- A skill with the same name as a command hides the command in Palette's list. That is fine when the skill hands off to the command's page or does what it does, as this skill does with the workspace's own `workspace-heal` page. Otherwise flag it.
- **Safe fix:** add an obvious missing row or pointer. Report a pointer whose page is gone.

### Instructions

- Instruction files that name a missing path, an old name or a command that no longer exists.
- Two instructions that would make the same task behave differently. Follow the more specific one, and report the conflict.
- Pointer files (`CLAUDE.md`, `GEMINI.md`, `.vibe/AGENTS.md`) point to `AGENTS.md` and copy none of its rules.

### Generated files

- A generated file, such as a dashboard rebuilt from Markdown, that is older than its sources, when the workspace says how it is built. Name the rebuild step. In report mode, don't run it.
- In fix mode, run a rebuild only after reading what it does. One that contacts an outside system, installs something or rewrites a wide area needs the person's yes first.

### When the workspace has no rules

Check only what holds anywhere: broken local links, paths left behind by a move, setup markers that are clearly active (not examples), instructions that conflict, and generated or dependency files mistaken for source.

When a real problem shows, add a short **Foundations to consider**: a root `README.md` that says where to start, a `README.md` for a folder that is hard to find your way in, or one source for agent instructions that are scattered. Name the problem each one solves and give a short outline. These are suggestions, never health failures, never made without a yes, and never for a small workspace that is clear as it is.

## 5. Report

Start with one line on the workspace's health. Then:

- **Basis:** Core, own rules or none.
- **Scope:** what was checked, what was left out, and whether the check was complete. If it was partial, say what was not checked and why.
- **Decisions** first: what needs the person.
- **Safe fixes** next: what fix mode would change.
- **Optional** last: setup to finish, pages to review, tidying.

Each finding gives the path (and the line when it helps), what is wrong, the rule, and the smallest fix. Leave out empty groups. End with the counts: findings, safe fixes, decisions, optional.

If the workspace is healthy, say what was checked. Never invent a problem to fill the report. Nothing is sent to a connected system.

## 6. Fix

In fix mode:

1. Say in one line what you will change.
2. Apply only the safe fixes above, within the scope asked for. Ask before any move, rename, deletion, overwrite or rewrite of content, unless the person already approved that exact change.
3. Keep the person's work and any unrelated changes. Stamp each page you changed with today's date and the acting person, as the conventions say.
4. Run the affected checks again. Say what changed, and what still needs a choice.
5. When the repairs mattered, add one dated line to the nearest existing `log.md`.

Never delete content, fill in facts, confirm drafts or create stubs to get a clean report.
