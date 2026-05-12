---
name: competitor-research
description: Research a single competitor and produce a structured profile. Use when adding a new competitor, refreshing an existing competitor's profile, or analyzing how a specific competitor positions against the user's product.
---

# Competitor Research

Use this skill when researching a specific competitor for the project's
market landscape.

## Where things live

Competitor profiles live in a `competitors/` folder under the project's
market directory. The conventional path is
`gtm/foundations/market/competitors/`, but check the project's actual
structure first — `landscape.md` in the parent folder is the synthesis
doc and tells you where everything lives.

When adding or significantly updating a profile, update `landscape.md`'s
tier table and threat assessment too — the synthesis is the load-bearing
part for decision-making.

## How to research

1. Use web search to gather current product info, pricing, recent news,
   and customer reviews. Marketing pages overstate; customer forums,
   review aggregators, and HN/Reddit threads tend to be more honest.
2. If the Palette MCP is available, pull the user's product context so
   the **Positioning** section can frame the comparison against the
   user's product specifically rather than describing the competitor in
   isolation.
3. Cross-check claims across sources before writing them down.

## Output structure

Match the existing `competitors/_template.md` shape (or whatever shape
the project's other competitor profiles use — read one first if you're
unsure). Default sections: positioning, pricing, strengths, weaknesses,
threat level, sources.

Always include a `**Last updated:**` date at the top so the user knows
when the profile was refreshed.
