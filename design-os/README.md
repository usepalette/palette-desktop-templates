# Design OS

Your design team as a file system: one folder of markdown for how the team thinks about design,
the calls it has settled, how the work is done, and what the design system is, with a folder
per designer for their drafts.

Built for design teams that work with AI agents, so a call one designer settles holds in the
next designer's work.

## What you get

- **Starter principles** for philosophy, progressive disclosure, page structure, layout,
  layering, typography, writing in the product, and naming. Your team changes them until they
  say what you believe.
- **Rules for settled calls**, one file per area: components, controls, spacing, surfaces,
  typography, icons, and motion. Each rule is dated with the reason for it, so it isn't argued
  again.
- **A design process** from exploring a problem to a scope engineering builds from, plus design
  reviews that write back what they settle.
- **Design system pages** for foundations and components, written from your code or design
  library. They say what each part is for and never copy token values, so they don't go out of
  date with what ships.
- **A folder per designer** with how they like to work and their drafts, so agents build on a
  teammate's earlier exploration instead of starting over.
- **Works with different AI agents.** `AGENTS.md` holds the shared rules, with small pointers
  that help Claude Code, Codex, Gemini, Mistral, and other supported agents work the same way.
- **Lessons and a log.** Corrections land in `lessons.md` and what happened in `log.md`. What
  repeats is proposed as a rule, and a person approves it.

## How setup works

Design OS starts with starter principles and process, empty rule files, and no sample data. Say
**"Set this up with me"** and tell the agent what you have:

- Whether you design in a design tool, in code, or both.
- Where your design system lives: a repo, a library, or a link.
- Where your product lives: a repo or a design file.
- Where your existing design docs are, if you have any.

A repo is enough to start. The agent adds you to `people/`, records where your team designs,
checks it can reach your repos and design files, writes the design system pages from your code
or library, and shows you where each existing doc would go before it writes anything. Pages it
writes stay marked "Not confirmed yet" until someone on the team has read them. Palette Desktop
creates a checkpoint first, so you can undo.

## Design from the same guidance

Open the folder with Claude Code, Codex, Gemini, or another supported agent. Every agent reads
the rules for the area it works in before it touches a UI.

- "Review this screen against our rules and principles."
- "We just settled that icons are always outlined. Add it as a rule."
- "Explore a new settings section from the problem up."
- "Break this design down into a scope for engineering."

Everything is plain markdown you can read and edit, with or without Palette.
