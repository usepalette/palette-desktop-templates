# Setting up Design

What the agent does in the session that installs this template. Read it with the template's README.

The app placed the Design space at `spaces/design/`, the design team's home inside the company OS. It holds how the team thinks about design (`principles/`), the calls it has settled (`rules/`), how the work is done (`process/`), what the design system is (`design-system/`), and the team's explorations (`drafts/`). Nothing was placed outside `spaces/design/`.

It ships as a **first version**: the principles are a first set marked "Not confirmed yet", the process pages are first drafts too, the rule files are empty, and the pages about the team's own setup (`repos.md`, `design-system/`) are marked "Not filled in yet". There is no sample data.

## What to do

1. **Say what it is.** Tell the person in one or two sentences what the Design space is. Don't read `AGENTS.md` or the README to them.

2. **If the install replaced a design space,** the app says so in its message. Say in one line that the earlier `spaces/design/` was replaced and that the checkpoint before the install still holds it. Offer to bring back pages from it, such as its `lessons.md`, `log.md` or rules, and copy them only after a yes. Never copy them without asking.

3. **Register the space**, the way `spaces/README.md` → Add a space, steps 7 and 8, describes. The space is already in place: don't copy `spaces/_template/` and don't recreate any of its files.
   - Its name is Design, its folder `spaces/design/`, and what it is for: the design team's principles, settled rules, process and design system. Its edit policy is `team`.
   - Its owner is the person installing unless they name someone else. Ask in the same round as the setup questions in step 5, not as a question of its own.
   - Add its row to the list of spaces in `spaces/README.md`, the area and its owner to **Areas and owners** in `company/how-we-work.md`, and one dated line to `spaces/log.md`. If either list already has a row for Design, which happens when this install replaced a design space, update that row; never add a second one.

4. **Stamp every page.** In each page under `spaces/design/` that has frontmatter, `[Owner]` becomes the owner, `last_updated` becomes today and `last_updated_by` becomes the person you are working for. Leave `drafts/_template/` as it is: it is a mold, and its slots are filled when a draft is made. Never change `template` in `spaces/design/README.md`: the app reads it to find the space and its version.

5. **Start the design setup now**, following `spaces/design/SETUP.md` as written. The person's profile is the one in the root `people/`; if they have none yet, the root rules make it. Then ask once for what they have: whether the team designs in a design tool, in code or in both, the design files and repos they work in, where the design system lives, and where their existing design docs are. Whatever they have is enough to start: a repo alone is fine. Show where each piece of existing material would go and write after their yes; never invent token names, components or decisions.

   A `SETUP.md` at the workspace root is the company's setup, separate from this one. If it is still running, the design space now counts as its first space.

6. **Sum up the first pass:**
   - Where the space is listed, and who owns it.
   - What you filled in, and which pages still say "Not filled in yet" or "Not confirmed yet" and need a person to read them.
   - That the first principles in `principles/` and the process in `process/` are there to be changed as the team works. They aren't part of setup.
   - How the guidance grows: a settled call becomes a rule in `rules/`, a correction goes into the space's `lessons.md`, and what happened goes into its `log.md`.

## Notes

- The root `AGENTS.md` always applies; `spaces/design/AGENTS.md` adds how to design, and the `CLAUDE.md` and `GEMINI.md` beside it point to it.
- Designers are people like everyone else: their profiles live in the root `people/`, never in the space. Their explorations go in `spaces/design/drafts/`.
- Production code and design files never live in this workspace. The repos and design files stay where they are, listed in `spaces/design/repos.md`. Repo access is personal: each designer follows `repos.md` → "Give agents access" on their own computer.
- `spaces/design/SETUP.md` is deleted when the design setup is done. Until then, the next agent to work in the space picks setup up where it stands.
