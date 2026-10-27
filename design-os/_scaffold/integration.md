# Design OS — install guide

You just installed Design OS into the user's workspace as a space, at `spaces/design/`: the design team's home inside the company OS. It holds how the team thinks about design (`principles/`), the calls it has settled (`rules/`), how the work is done (`process/`), what the design system is (`design-system/`), and the team's explorations (`drafts/`). Nothing was placed outside `spaces/design/`.

It ships as a **starter**: the principles are a starter set marked "Not confirmed yet", the process pages are starters too, the rule files are empty, and the pages about the team's own setup (`repos.md`, `design-system/`) are marked "Not filled in yet". There is no sample data.

## What to do

1. Tell the user briefly what Design OS is — one or two sentences. Don't read `AGENTS.md` or the README to them.

2. **Register the space**, the way `spaces/README.md` → Add a space, steps 7 and 8, describes. The space is already in place: don't copy `spaces/_template/` and don't recreate any of its files.
   - Its name is Design, its folder `spaces/design/`, and what it is for: the design team's principles, settled rules, process and design system. Its edit policy is `team`.
   - Its owner is the person installing unless they name someone else. Ask in the same round as the setup questions below, not as a question of its own.
   - Add its row to the list of spaces in `spaces/README.md`, the area and its owner to **Areas and owners** in `company/how-we-work.md`, and one dated line to `spaces/log.md`. Stamp `owner`, `last_updated` and `last_updated_by` on `spaces/design/README.md`.
   - If `spaces/design/AGENTS.md` is not among the files this install placed, the workspace already had a design space, and its own `README.md`, `AGENTS.md` and memory files were kept. Don't register it again: tell the user, and offer to bring the Design OS rules from the files that did land into that space's `AGENTS.md`.
   - If the workspace has no `spaces/README.md`, it wasn't set up from Company OS. Skip the registration, tell the user the design space is in `spaces/design/` with its rules in `spaces/design/AGENTS.md`, and offer to add a line pointing to it from their root `AGENTS.md`.

3. **Start the design setup now**, following `spaces/design/SETUP.md` as written. The user's profile is the one in the root `people/`; if they have none yet, the root rules make it. Then ask once for what they have: whether the team designs in a design tool, in code or in both, the design files and repos they work in, where the design system lives, and where their existing design docs are. Whatever they have is enough to start — a repo alone is fine. Show where each piece of existing material would go and write after their yes; never invent token names, components or decisions.

   A `SETUP.md` at the workspace root is the company's setup, separate from this one. If it is still running, the design space now counts as its first space.

4. After the first pass, give a quick summary:
   - Where the space is listed, and who owns it.
   - What you filled in, and which pages still say "Not filled in yet" or "Not confirmed yet" and need a person to read them.
   - That the starter principles in `principles/` and the process in `process/` are there to be changed as the team works — they aren't part of setup.
   - How the guidance grows: a settled call becomes a rule in `rules/`, a correction goes into the space's `lessons.md`, and what happened goes into its `log.md`.

## Notes

- The root `AGENTS.md` always applies; `spaces/design/AGENTS.md` adds how to design, and the `CLAUDE.md` and `GEMINI.md` beside it point to it.
- Designers are people like everyone else: their profiles live in the root `people/`, never in the space. Their explorations go in `spaces/design/drafts/`.
- Production code and design files never live in this workspace — the repos and design files stay where they are, listed in `spaces/design/repos.md`. Repo access is personal: each designer follows `repos.md` → "Give agents access" on their own computer.
- `spaces/design/SETUP.md` is deleted when the design setup is done. Until then, the next agent to work in the space picks setup up where it stands.
