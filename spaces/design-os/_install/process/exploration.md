---
type: doc
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
read_when:
  - You are starting a new product, a new section, or a screen that needs rethinking from the problem up
---

# Exploration

How a design exploration runs, from the data underneath to a pitch for the result. The steps run in order and each ends in a short doc, so the reasoning behind a design can be read back later. The first five are understanding and contain no UI. A screen designed before the problems are ranked is designed for whichever problem came to mind first.

## The steps

1. **Data model** — List what the product holds: the entities, what each carries, how they relate, where each comes from and the states it moves through. Start from the real schema and pull a real sample. Note the cuts the data supports, such as time, category, person and state, and what the data does not contain
2. **Derived data** — Write what can be calculated from it, as the question each value answers, with how sure it is: exact, estimated or a guess the person confirms. Exceptions are usually worth the most, because the norm carries no information
3. **Users** — Name the groups by what they are trying to get done, and rank them. One primary group, whose needs win every conflict. Secondary groups are served where it costs the primary nothing. List each group's needs from their side, and read a feature request for the need underneath it
4. **Scenarios** — Write the real moments a need comes up, as short stories: what happened before, what they open the product to do, what they leave with. Name the mindset of each, such as checking, worried, planning, reviewing or setting up. Cover the first time, an ordinary week and the week something goes wrong. Then strip the problem to what stays true however it is solved, and check each convention in the category against that
5. **Problems** — Walk each scenario and write where it breaks today. Rank by how often it happens, how much it hurts and how many primary users have it, and draw a line under what this exploration solves. Group the problems into modalities, the way a person would expect to find them in one place
6. **Solutions** — Write the bare minimum that solves each problem above the line, in one sentence, starting from what the product already has. Cut edge cases on purpose. Every addition is its own decision, and the doc keeps two lists that never mix: in scope, and captured but not in scope
7. **Information architecture** — Turn the modalities into the main places, each with one job and a name a person would use. Put every solution in one place, at the depth that matches how often it is used. Walk every scenario through the structure and fix where a person would go to the wrong place first
8. **Designing** — Branch out into eight distinct versions, each a different answer to the same problem, built quickly with real data and shown side by side. Simplify the strongest over five levels: decoration, distractions, secondary data, labels the shape already says, then only what the main scenario needs. Refine the best of both into one design, with the team's tokens and components, across every state from empty to full
9. **Pitch** — Write why the experience makes sense, in the owner's words: the concept in a paragraph or two, then each part with its moment, what the person gets, why it matters to them and why it matters to the business. No states, no edge cases and no selling

## Going back

Later steps send you back to earlier ones. A scenario turns up data the model is missing; a branch in step 8 shows a problem was ranked too low. Update the earlier doc, so the docs always agree.

## Where the person decides

An agent can run a step alone and bring the doc back. It stops and waits where a step ends in a decision that belongs to the person who owns the design.

- **Ranking users** — Who is primary decides every conflict later
- **Ranking problems** — Decides what gets designed first
- **Adding scope** — Every addition beyond the bare minimum
- **Picking from the branches** — Which versions go on to be simplified
- **The recommendation** — The refined design that goes into the pitch

Everywhere else, the agent picks a sensible default, writes it down and moves on.

## The docs

One folder per exploration, in the draft or project it belongs to. The docs are named by subject.

```
data.md          the data model and what is derived from it
users.md         users ranked, with their needs
scenarios.md     moments, mindsets, first principles
problems.md      problems ranked and grouped into modalities
solutions.md     one minimum solution per problem, with what is left out
structure.md     the main places and where each solution lives
<subject>.md     one doc per design subject, with its branches and levels
pitch.md         the concept and each part, in the owner's words
```

The branches and prototypes live in the repo, on the draft's branch, or in the design file, linked from the subject doc. A small exploration folds the docs into one, with a section per step. Every step is still walked through.

When the pitch is accepted, the design is broken down for engineering in a [scope document](scope-documents.md). Parts are named per [`naming.md`](../principles/naming.md) from step 6 on, so the names in the exploration, the scope and the design file are the same.
