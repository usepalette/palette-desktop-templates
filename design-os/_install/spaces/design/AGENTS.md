# design

The design space inside the company OS: how the team thinks about design, the calls it has settled, how the work is done and what the design system is, plus the drafts of what designers are exploring. **Company-wide rules live in the root [`AGENTS.md`](../../AGENTS.md) and always apply**; this file adds how to think and behave here. For what lives where, see [`README.md`](README.md).

## Posture

Work as a designer on the team who knows the system, the code and the people. This space exists so that what one designer learns is there for the next one: a call settled in one person's exploration is a rule the same day, and every agent reads the rules before it touches a UI.

## Before design work

The root rules say who the person is and what to read first. Then, in this order:

1. **If `SETUP.md` exists in this folder, read it.** The design space is still being set up. Setup never blocks the task the person came with.
2. **For any design or UI work**, read [`rules/README.md`](rules/README.md) and the rule files for the areas the work touches, then the principle for what you are doing (the list is in [`principles/README.md`](principles/README.md)), then the design system pages for the components and foundations you will use.
3. **For any work in code or a design file**, read [`repos.md`](repos.md), check that the repo you need is reachable, and read that repo's own `AGENTS.md`, `CLAUDE.md`, `README.md` and contributing guide before changing anything. For a design file, read the team's rules for it, such as `rules/figma.md`, if there are any.

## Where the design happens

**This team designs [in a design tool | in code | in both].** Setup fills in this line. Until it is filled in, ask the person once and work the way they answer.

- **In a design tool** — Design work happens in the team's design files, built from the library's components and variables. A draft's `README.md` links the file and the page. Read the library before drawing, and the shipped code when the agent can reach it, since the code is what ships.
- **In code** — Design work happens in the real repo, on a branch of its own, with the shipped components, tokens and data. Create the branch before changing anything, never work on the main branch, and commit, push or open a pull request only when the person asks. Code lives in a draft folder only when the person asks for a standalone prototype.
- **In both** — The person says where each draft starts. A draft that moves from the design file to code links both. When the design file and the code disagree, say so, and the person decides which one changes.

The rest holds wherever the work happens.

- **Read what exists, never remember it.** Tokens, components and patterns are read from the code or the design library; never name a token, a component or a prop from memory. When a page here and the shipped product disagree, say so: either the product changes on purpose, or the page does.
- **Systems before one-offs.** Use the team's tokens and components. No hardcoded colours, sizes, spacing or font weights. If a value or a pattern repeats, it belongs in the design system, so propose adding it there.
- **Extend a component, never build around it.** When a component cannot do what a screen needs, propose the variant, the slot or the property it is missing, in the design system, for every screen that uses it.
- **Look for earlier work before you start.** Search [`drafts/`](drafts/README.md) and the projects in [`projects/`](../../projects/README.md) for the same component, screen or problem. Build on what a teammate already tried, and link to it.
- **Repo rules win for code.** A repo's own instruction files and conventions decide how code is written there. This space decides how things are designed.
- **Editable repos and files change for real.** A change in a repo or a design file the agent can write to happens there directly, outside any review of this workspace. Say what you will change before you change it.

## Rules

- **Cite the guidance.** When a design decision matters, name the principle or the rule behind it, so the next person can follow the reasoning.
- **Start from the company context.** The brand's look is in [`company/brand/design.md`](../../company/brand/design.md), its voice in [`company/brand/voice.md`](../../company/brand/voice.md) and the products in [`company/products/`](../../company/products/README.md). Link to them; never copy them here. This space holds the product's design.
- **Follow a process when one exists.** Exploring a problem, scoping a design for engineering and reviewing one each have a page in [`process/`](process/README.md); use it.
- **Before you finish,** update the `README.md` of the draft or project you worked on: where it stands, and the link to the branch or pull request if there is one.

## Bringing design material in

The root rules for bringing material in apply: show where each piece would go, wait for a yes, never overwrite what a page says, and pages written from it stay **Not confirmed yet**. Design material sorts like this:

- **A belief about design** — [`principles/`](principles/README.md)
- **A specific decision** — the rule file for its area in [`rules/`](rules/README.md)
- **An explanation of a token or a component** — [`design-system/`](design-system/README.md)
- **A code convention** — that repo's notes in [`repos.md`](repos.md)
- **A step in how the team works** — [`process/`](process/README.md)
- **The brand's look or voice** — [`company/brand/`](../../company/brand/README.md), not here

## Share what you learn

This is the part that makes each designer's work improve the others'. When something durable comes out of a session, write it down in the same session, in the narrowest place that is useful to others.

| What came out of the work | Where it goes |
|---|---|
| A settled design call that should hold next time: an icon style, a button treatment, a spacing rule, a copy rule | a rule in the area file in [`rules/`](rules/README.md), and a line in this space's [`log.md`](log.md) |
| A correction about using the design system or the guidance | this space's [`lessons.md`](lessons.md) |
| A correction about a repo: a build step, a gotcha, a convention | the repo's notes in [`repos.md`](repos.md) |
| Where an exploration stands, and what it taught | its `README.md` in [`drafts/`](drafts/README.md) |
| What happened, or what was decided, in design | this space's [`log.md`](log.md) |

How to work with one person, and anything about one project, goes where the root rules say: that person's or that project's own files.

The bar is "would a teammate doing this next month want to know?" Capture that, skip the trivial. A new rule is shown to the person first and written after their yes.

**Promote what repeats.** When the same lesson shows up more than once, propose turning it into a rule and removing the copies. When a rule has become a way of thinking, propose moving it into its principle. Propose it; a person approves.

## Where to read for a task

| When the task is… | Read |
|---|---|
| Setting up the design space, or a designer joining | `SETUP.md` if it exists, then [`repos.md`](repos.md) → Give agents access |
| Bringing existing design docs in | "Bringing design material in" above, then the README of each folder the material goes to |
| Exploring a new product, section or screen | [`process/exploration.md`](process/exploration.md) |
| Designing a screen or component | the rule files for its areas, [`principles/`](principles/README.md), then [`design-system/`](design-system/README.md) |
| Reviewing a design | [`process/reviews.md`](process/reviews.md) |
| Breaking a design down for engineering | [`process/scope-documents.md`](process/scope-documents.md) |
| Writing or changing UI code | [`repos.md`](repos.md), then the repo's own instruction files |
| The words on a screen | [`principles/writing-in-the-product.md`](principles/writing-in-the-product.md) |
| An exploration in progress | its folder in [`drafts/`](drafts/README.md), then the branch or the design file it links |

Keep this file short. Detail belongs in the pages it links to.
