---
type: command
owner: Shared
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: everyone
description: "Check the workspace for broken links, lists that no longer match, pages nobody has confirmed and scratchpads that have piled up. Reports first"
argument-hint: "[report|fix]"
---

# Workspace heal

Check structure, links, metadata and unfinished content. Say "check the workspace" or "is anything broken?". Report mode is the default and changes nothing. Fix mode applies only the requested safe repairs. Scheduling requires an explicit request; scheduled runs report only.

Read [conventions](../conventions.md) and [page states](../page-states.md). Collect findings once and report decisions first.

## Checks and permitted fixes

### Links

Every real local Markdown link must resolve, including heading anchors where used. Skip web URLs and placeholder destinations. Backtick paths containing `<name>` or `[Space]`, examples and explicitly conditional future paths are patterns, not broken links.

**Fix:** repair a destination only when it is unambiguous and within the request. Otherwise show the choices; don't create a stub.

### Lists and maps

Real items in people, spaces, customers and projects must match their collection indexes. Product, competitor, format and command files must match their lists. Exclude molds and standard furniture (`README.md`, applicable rules/pointers and memory files) from item counts; the commands README does not list itself.

Trees must match the retained structure. Exclude explicit on-first-use paths, example space names and temporary `SETUP.md` after setup. When a folder was deliberately removed, check that both links and dependent procedures were adjusted.

**Fix:** add or remove clearly stale index rows. Never infer a business status merely to fill a table.

### Placement

Flag working files in the root, orphaned work with no clear home, and meeting notes outside their expected destination. The documented scratchpad meeting fallback is valid. A marked draft beside confirmed pages is valid. Check heavy files against the storage arrangement in `company/tools.md`.

**Fix:** propose a move unless already authorized; update links with it.

### Page state and setup

List unfilled pages, unconfirmed drafts and claims marked "(to confirm)"; separate optional completion work from defects. Read the four core setup pages first when setup is active.

Editorial review and record lifecycle are separate. A confirmed exploratory project may be `draft`; an active record may contain a new section awaiting review. Navigation, procedures and empty memory files need no review box. Optional unknown profile fields and slots in reusable formats are intentional.

When `SETUP.md` exists, apply its five-part test: four existing, confirmed core pages and a first space, or an explicit decline of that space. A missing required page is not completed setup.

**Fix:** never confirm content on the person's behalf. Offer a named batch for review when useful.

### Frontmatter

Every content Markdown file needs valid frontmatter and `type`; folder READMEs and substantial documents need the full block in conventions. Small leaves follow their mold's schema. `AGENTS.md` and vendor pointer files intentionally have no frontmatter; HTML is not Markdown.

Real workspace edits need a date and verified human attribution, never an agent name. Unknown owners remain unknown. Untouched seed dates and authors, and preserved mold slots, are intentional.

**Fix:** add an obvious missing type or other known metadata within the requested scope. Stamp changes actually made with today's date and the acting person; don't invent ownership or historical dates.

### Furniture

The root, top-level content folders, real spaces and people have README, lessons and log files. Deeper content folders need a README but inherit the nearest existing memory pair. Technical host folders need no content furniture; `.agents/` has its reference index but needs no memory pair.

Customer and project copies include their meetings README and mold, with real navigation headings and stamps. A space's meetings folder has both files when created. Retained collections of repeated items keep their molds. Local space rules have the appropriate vendor pointers; removing optional rules also removes their README references.

**Fix:** flag incomplete copies. Restore missing pieces only when authorized, preserving existing content. Don't invent local rules or fill unknown facts.

### Memory

Flag lessons longer than about twenty entries, duplicate or contradictory lessons, history in lessons, rules in logs and ambiguous relative dates. Sensitive details do not belong in broad README, lessons or log surfaces. Do not repeat those details in the report.

**Fix:** resolve an unambiguous relative date within scope. Use the reflect procedure for proposed rule consolidation; ask about confidential storage under the root rule.

### Scratchpads

Check each index against its files. List older work for its owner to keep, promote or delete. Multiple versions and external links into a scratchpad are review signals, not proof that something should move.

**Fix:** repair index rows within scope. Don't delete or move another person's work without authority.

### Commands

Each page in `.agents/commands/`, except `README.md`, has an index row and a pointer file with the same name in `.claude/commands/`, and each pointer names a page that exists. The procedure lives in the page, never in the pointer.

**Fix:** add an obvious missing row or pointer; report a pointer whose page is gone.

## Report

Give the findings in the conversation, with decisions first, then safe repairs, then optional setup or cleanup. Include exact paths, the issue and suggested fix; omit empty categories. In fix mode, distinguish what changed from what still needs a choice. Nothing is sent to a connected system. Add a short line to the nearest existing log only when meaningful repairs were made.
