# Design OS — install guide

You just installed Design OS into the user's workspace — the shared home of a design team that
works with agents: one folder of markdown for how the team thinks about design (`principles/`),
the calls it has settled (`rules/`), how the work is done (`process/`), what the design system
is (`design-system/`), and one folder per designer with their drafts (`people/`).

It ships as a **starter**: the principles are a starter set marked "Not confirmed yet", the
process pages are starters too, the rule files are empty, and the pages about the team's own
setup (`repos.md`, `design-system/`) are marked "Not filled in yet". There is no sample data.

## What to do

1. Tell the user briefly what Design OS is — one or two sentences. Don't read `AGENTS.md` or the
   README to them.

2. Start setup now, following `SETUP.md` (already placed) as written. It makes the user's folder
   in `people/`, then asks once for what they have: whether the team designs in a design tool,
   in code or in both, the design files and repos they work in, where the design system lives,
   and where their existing design docs are. Whatever they have is enough to start — a repo
   alone is fine. Show where each piece of existing material would go and write after their
   yes; never invent token names, components or decisions.

3. After the first pass, give a quick summary:
   - What you filled in, and which pages still say "Not filled in yet" or "Not confirmed yet"
     and need a person to read them.
   - That the starter principles in `principles/` and the process in `process/` are there to be
     changed as the team works — they aren't part of setup.
   - How the guidance grows: a settled call becomes a rule in `rules/`, a correction goes into
     the nearest `lessons.md`, and what happened goes into `log.md`.

## Notes

- `AGENTS.md` is the source of truth for how agents behave here; `CLAUDE.md`, `GEMINI.md` and
  `.vibe/AGENTS.md` are thin pointers to it.
- Production code and design files never live in this workspace — the repos and design files
  stay where they are, listed in `repos.md`. Repo access is personal: each designer follows
  `repos.md` → "Give agents access" on their own computer.
- `SETUP.md` is deleted when setup is done. Until then, the next agent to open the folder picks
  setup up where it stands.
