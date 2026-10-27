# Design OS

A design space for your workspace: one folder of markdown for how your team thinks about design,
the calls it has settled, how the work is done, and what the design system is, with a folder
for each exploration.

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
- **Shared drafts**, one folder per exploration with who owns it and where it stands, so agents
  build on a teammate's earlier work instead of starting over.
- **Lessons and a log for design.** Corrections land in the space's `lessons.md` and what
  happened in its `log.md`. What repeats is proposed as a rule, and a person approves it.

## Part of your workspace

Design OS installs as a space, `spaces/design/`, next to your other spaces. It doesn't replace
anything already there:

- Your workspace's rules still apply. The space's own `AGENTS.md` adds how to design, and agents
  read it whenever they work in the space.
- Designers use their profile in `people/`, like every teammate.
- The space links to your brand and products in `company/` instead of copying them.

## How setup works

After install, the agent adds Design to your list of spaces and starts its setup. Tell it what
you have:

- Whether you design in a design tool, in code, or both.
- Where your design system lives: a repo, a library, or a link.
- Where your product lives: a repo or a design file.
- Where your existing design docs are, if you have any.

A repo is enough to start. The agent records where your team designs, checks it can reach your
repos and design files, writes the design system pages from your code or library, and shows you
where each existing doc would go before it writes anything. Pages it writes stay marked "Not
confirmed yet" until someone on the team has read them. Palette Desktop creates a checkpoint
first, so you can undo.

## Design from the same guidance

Agents working on design read the space's rules for the area before they touch a UI.

- "Review this screen against our rules and principles."
- "We just settled that icons are always outlined. Add it as a rule."
- "Explore a new settings section from the problem up."
- "Break this design down into a scope for engineering."

Everything is plain markdown you can read and edit, with or without Palette.
