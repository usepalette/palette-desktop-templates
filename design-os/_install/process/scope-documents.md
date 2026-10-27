---
type: doc
read_when:
  - You are turning a design, a prototype or an idea into a scope that engineering builds from
---

# Scope documents

A scope document says what a person sees and does in one piece of the product, and what happens when they do it. Engineering builds from it. Every behaviour a developer would otherwise have to guess is written down, or listed as an open question with a name on it.

## What a scope covers

What is on the screen, what each control does, the states, the keys, what is remembered and for how long, and what happens at the edges. How it is built, how fast it runs and what data it needs stay out.

Components are the one technical thing a scope names. Which design system component a part is built from is a design decision, so the scope says it.

## Where it lives

In the draft or project folder it belongs to.

- **One part** — One file named for its subject
- **Several parts** — A `scope/` folder with a `README.md` and one numbered file per part, in the order they get built

## Sections

In this order, and only the ones the scope has something for.

- **Opening paragraph** — What the person gets, and where the design comes from, with a link to the branch or design file
- **What the product does today** — The shipped behaviour this changes, read from the code
- **In this scope** — The parts, one line each
- **Out of this scope** — The neighbouring parts that stay as they are, so nobody builds them by accident
- **A section per part** — What it shows, what a person can do and what follows
- **States** — Every state of the part, the empty and the failing ones included
- **Design system** — Which component each part is built from, and what is new
- **Decisions** — The calls made while scoping
- **Open questions** — One line each, with who answers

## Writing a part

- **Elements** — A list of what is on it, `**Name** — Description`
- **Behaviour** — A condition and what follows: "Clicking a result ends the search"
- **Input** — Click, keyboard, Escape, hover, focus and clicking outside, each where it applies
- **Memory** — What is kept, where, and when it is forgotten
- **Copy** — The real words, in quotes, per [`writing-in-the-product.md`](../principles/writing-in-the-product.md)
- **Numbers** — Only where the number is the decision

A part that only looks right in its good state is not finished. The states cover empty, loading, failed, nothing matches, long names, many items and no access, for each one the part can reach.

## Structure on screen

Settle where the thing sits before writing the parts.

- **Zone** — Header, content or navigation, per [`page-structure.md`](../principles/page-structure.md)
- **Layer** — Whether it opens on top of something, and which kind, per [`layering.md`](../principles/layering.md)
- **Depth** — What shows first and what is one level deeper, per [`progressive-disclosure.md`](../principles/progressive-disclosure.md)
- **Grouping** — How the elements group and space, per [`layout-and-composition.md`](../principles/layout-and-composition.md)

Check the [rules](../rules/README.md) before proposing anything they already settle.

## Design system

Each part names the component it is built from, by its name in the package. The design system section lists every component the scope uses, in these groups, in order of preference.

- **Used as it ships** — The component and the props it takes
- **Changed in the design system** — A variant or a part the component does not have yet, and what changes
- **New** — Nothing in the package does the job, and why the nearest component does not fit

A change or a new component goes into the design system for every screen that uses it. A one-off built inside one screen is not an option. A new component gets a doc in [`../design-system/components/`](../design-system/components/README.md), and the scope links to it.

## Decisions and open questions

A decision is written `**Name** — Description` and says what was chosen. If it changes an earlier document, the scope names that document and what it said before.

An open question is one line: the subject in bold, the question, and who answers it. A question with nobody to answer it is not finished.
